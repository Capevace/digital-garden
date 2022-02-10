# Create Node CLI
#dev 

## Entry file

```js
#!/usr/bin/env node

// ... Code
```


## Make the file executable

```bash
chmod +x cli.js
```


## Package.json

```json
{
	"bin": {
		"<cmd-name>": "./path/to/entry.js"
	}
}

```