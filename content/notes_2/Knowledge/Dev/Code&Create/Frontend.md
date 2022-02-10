https://github.com/bumbu/svg-pan-zoom


## Get circle data
```js
$$('circle')
	.map(circle => ({ 
		id: circle.getAttribute('id'), 
		x: circle.getAttribute('cx'), 
		y: circle.getAttribute('cy'),
		properties: [],
		disabled: false,
		bookable: true,
		booked: []
	}));
```
