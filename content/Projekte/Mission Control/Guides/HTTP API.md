\#mission-control #docs

# HTTP API Guide

The HTTP API can be used in plugin initializers and is available in the [PluginAPI](Creating%20first%20plugin.md#plugin-api).

*Example:*

````js
// File: my-plugin/index.js
module.exports = function initPlugin({ config, http }) {
	// Create a route at /plugins/my-plugin/hello-world
	http.get('/hello-world', (req, res) => {
		res.json({
			message: 'Hello World!'
		});
	});

	// /plugins/my-plugin/assets -> Files from ..../my-plugin/resources/
	http.use(
		'/assets',
		express.static(__dirname + '/resources')
	);
}
````

Plugins can use the HTTP API to accept custom HTTP endpoints.

 > 
 > **NOTE:** You won't need to create custom HTTP endpoints for service data. See [Service API > HTTP endpoints](Service%20API.md#http-endpoints).

There are three `express.Router` routers to register routes on:

## Contents

* [Available HTTP Routers](HTTP%20API.md#available-http-routers)
  * [http](HTTP%20API.md#http-httpcontext-extends-httprouter)
  * [http.root](HTTP%20API.md#http-root-httprouter)
  * [http.unsafeRoot](HTTP%20API.md#http-unsaferoot-httprouter)
* [HTTP Router API](HTTP%20API.md#http-router-api)
  * [router.baseUrl](HTTP%20API.md#router-baseurl-string)
  * [router.proxy](HTTP%20API.md#http-proxy-route-target-options)

---

## Available HTTP Routers

### http: `HTTPContext` *extends* `HTTPRouter`

*Root URL:* `/`
*Authentication required*

The `http` object itself extends `express.Router`.

These routes will be prefixed with the plugins URL root: `/plugins/PLUGIN-NAME/`.
Authentication is required for these routes, and permission checks are automatically performed.
This means a user object is a given when handling these requests.

*Example*: 

````js
// File: my-plugin/index.js

// Create a post route at /plugins/my-plugin/random-number
http.post('/random-number', (req, res) => {
	res.json({
		number: Math.random()
	});
});
````

---

### http.root: `HTTPRouter`

*Root URL:* `/`
*Authentication required*

This HTTP router listens at the HTTP root `/` so routes will be available at `https://mission-control.local/...`.

Authentication is also required for these routes, and permission checks are automatically performed.
This means a user object is a given when handling these requests.

*Example*: 

````js
// File: my-plugin/index.js

// Create a authenticated post route at /random-number
http.root.post('/random-number', (req, res) => {
	res.json({
		number: Math.random()
	});
});
````

---

### http.unsafeRoot: `HTTPRouter`

 > 
 > **Warning**: 
 > Authentication will not be required by default! These routes are **PUBLIC.**

*Root URL:* `/`

This HTTP router listens at the HTTP root `/` so routes will be available at `https://mission-control.local/...`.

Authentication is also required for these routes, and permission checks are automatically performed.
This means a user object is a given when handling these requests.

*Example*: 

````js
// File: my-plugin/index.js

// Create a UNSAFE post route at /random-number
http.unsafeRoot.post('/random-number', (req, res) => {
	res.json({
		number: Math.random()
	});
});
````

---

## HTTP Router API

### router.baseUrl: `String`

The router's base URL.
The `config.http.url` value will be used for this.
*Unless the `http.root / http.unsafeRoot` router is used, URLS will be prefixed with `/plugins/PLUGIN-NAME`.*

---

### http.proxy(route, target, \[options\])

Proxy an HTTP request to another target URL

This is useful if you want to proxy another service through mission-control, for example `homebridge-config-ui-x` or a similar webapp.

The options are passed to `http-proxy-middleware` directly, which is the proxy implementation used.

*Example:*

````js
// File: my-plugin/index.js

// Create a post route at /plugins/my-plugin/do-something
http.proxy('/homebridge', 'http://localhost:8080' {
	onProxyReq(proxyReq, req) {
		// pass user to service
		if (req.user)
			proxyReq.setHeader('X-Auth-User', req.user.username);
	}
});
````
