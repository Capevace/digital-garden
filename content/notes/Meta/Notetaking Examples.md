---
date updated: '2021-05-10T01:07:17+02:00'

---

## Page Breaks

Put this where you want it to break:

```html
<div style="page-break-after: always;"></div>
```

---


## Embed PDF

````
```pdf
{
	url: "[[Projektdokumentation.pdf]]"
}

````

```pdf
{
	"url": "[[Projektdokumentation.pdf]]",
	"scale": 0.4
}

```


| parameter | required                       | example                                                      |
| --------- | ------------------------------ | ------------------------------------------------------------ |
| url       | yes                            | **myPDF.pdf** or **subfolder/myPDF.pdf** or "[[MyFile.pdf]]" |
| page      | optional (default = 1)         | **1** or **[1,6,7,8]**                                       |
| scale     | optional (default = 1.0)       | **0.5** for 50% size or **2.0** for 200% size                |
| rotation  | optional (default = 0)         | **90** for 90deg or **-90** -90deg or **180**                |
| rect      | optional (default = [0,0,0,0]) | offsetX, offsetY, sizeX, sizeX in Pixel                      |

## Table

| Hello | What | How |
| ----- | ---- | --- |
| How   |      |     |

## Info Blocks

Format:

````
```ad-note
title: test
collapse: false

````

### Types

| Type     | Aliases                     |
| -------- | --------------------------- |
| note     | note, seealso               |
| abstract | abstract, summary, tldr     |
| info     | info, todo                  |
| tip      | tip, hint, important        |
| success  | success, check, done        |
| question | question, help, faq         |
| warning  | warning, caution, attention |
| failure  | failure, fail, missing      |
| danger   | danger, error               |
| bug      | bug                         |
| example  | example                     |
| quote    | quote, cite                 |

### Block Examples

```ad-note
```

```ad-abstract
```

```ad-info
```

```ad-tip
```

```ad-question
```

```ad-success
```

```ad-warning
```

```ad-failure
```

```ad-danger
```

```ad-bug
```

```ad-example
```

```ad-quote
```


```leaflet
id: leaflet-map
height: 500px
lat: 50
long: 50
height: 500px
minZoom: 1
maxZoom: 10
defaultZoom: 5
unit: meters
scale: 1
marker: default, 39.983334, -82.983330, [[HTTP API]]
darkMode: true
```