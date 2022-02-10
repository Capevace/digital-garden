#mission-control #docs

# Sync / Service API Guide

The HTTP API can be used in plugin initializers and is available in the `PluginAPI`.

*Example:*
```js
// File: my-plugin/index.js
module.exports = function initPlugin({ config, http }) {
	// Create a route at /plugins/my-plugin/hello-world
	http.get('/hello-world', (req, res) => {
		res.json({
			message: 'Hello World!'
		});
	});

	// /plugins/my-plugin/assets -> Files from /resources
	http.use(
		'/assets',
		express.static(__dirname + '/resources')
	);
}
```

Plugins can use the HTTP API to accept custom HTTP endpoints.

> **NOTE:** You won't need to create custom HTTP endpoints for service data. See [Service API > HTTP endpoints](service-api.md#http-endpoints).

There are three `express.Router` routers to register routes on:

## Contents
- [HTTP Routers](#http-routers)
	- [http](#http--httpcontext-extends-httprouter)
	- [http.root](#httproot--httprouter)
	- [http.unsafeRoot](#httpunsaferoot--httprouter)
- [HTTP Router API](#http-router-api)
	- [router.baseUrl](#routerbaseurl--string)
	- [router.proxy](#httpproxy-route-target--options--)

## Sync Concepts – Services & actions

Concept


## Transports

Sync

### Socket.io transport


### HTTP endpoints
