# blocks
blocks are the cool little boxes that you can insert into a [beta](https://beta.wasteof.money) or [alpha](https://alpha.wasteof.money) profile's sidebar.

there are currently 7 different types of blocks that you can place into your sidebar, those being:
- statistics (`StatsBlock`)
- links (`LinksBlock`)
- a youtube video (`YoutubeBlock`)
- text (`TextBlock`)
- featured users (`FeaturedUsersBlock`)
- a featured post (`PostBlock`)
- (ALPHA ONLY) a scratch project (`ScratchProject`)

in case this is helpful to anyone reading this, here's also a list of their json equivalents:
```json
{
	"type": "StatsBlock",
	"data": {
		"title": "Statistics"
	}
}
```

```json
{
	"type": "LinksBlock",
	"data": {
		"title": "Links",
		"links": [
			{
				"text": "Google",
				"url": "https://www.google.com"
			}
		]
	}
}
```

```json
{
	"type": "YoutubeBlock",
	"data": {
		"title": "A YouTube Video",
		"video": "dQw4w9WgXcQ"
	}
}
```

```json
{
	"type": "TextBlock",
	"data": {
		"title": "Text",
		"text": "This is some text."
	}
}
```

```json
{
	"type": "FeaturedUsersBlock",
	"data": {
		"title": "Featured users",
		"users": [
			"60c4976b59c622b5661559c4"
		]
	}
}
```

```json
{
	"type": "PostBlock",
	"data": {
		"title": "Featured post",
		"post": "60c4976b59c722b5661559c4"
	}
}
```

(ALPHA ONLY!!)
```json
{
	"type": "ScratchBlock",
	"data": {
		"title": "A Scratch Project",
        "project": "16795490"
	}
}
```

## side note
blocks also contain a `dndID` key within their JSON. this key stands for "drag and drop ID" and is always set to a random value using the `Math.random` function.

so really, a more accurate version of a block's JSON would look something like this:
```json
{
	"dndID": 0.8421870702311771, // Math.random()
	"type": "TextBlock",
	"data": {
		"title": "text",
		"text": "plaintext string here"
	}
}
```
but this `dndID` key isn't necessary in most cases, so it has been stripped out.