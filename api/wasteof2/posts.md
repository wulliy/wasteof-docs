# posts

- `/posts/:id`
	```
	method: GET
	example: /posts/60c4d33f1ea77fed94251ab7

	-----------
	returns the post with the specified id.
	-----------

	method: PUT
	-----------
	edits the post with the specified id.

	the contents of the post will be replaced with whatever value is in the
	"post" key in the request's body.
	-----------
	
	method: DELETE
	-----------
	deletes the post with the specified id.
	-----------
	```

- `/posts/:id/comments`
	```
	method: GET
	example: /posts/60c4d33f1ea77fed94251ab7/comments

	-----------
	returns the comments of a post with the specified id.

	an additional `?page` URL parameter can be added to fetch the comments on that
	page.
	-----------

	method: POST
	body: {
		"content": "<p>comment</p>",
		"parent": null
	}
	example: /posts/60c4d33f1ea77fed94251ab7/comments

	-----------
	creates a comment/reply under a post with the specified id.
	-----------
	```

- `/comments/:id/replies`
	```
	method: GET
	example: /comments/60c4d33f1ea77fed94251ab7/replies

	-----------
	returns the replies of a comment with the specified id.

	an additional `?page` URL parameter can be added to fetch the replies of the
	comment on that page.
	-----------
	```

- `/posts/:id/pin`
- `/posts/:id/unpin`
	```
	method: POST
	example: /posts/60c4d33f1ea77fed94251ab7/pin

	-----------
	pins/unpins the post with the specified id.
	-----------
	```

- `/posts/:id/report`
	```
	method: POST
	body: {
		"type": "none",
		"reason": "report reason"
	}
	example: /posts/60c4d33f1ea77fed94251ab7/report

	-----------
	reports the pin with the specified id.
	-----------
	```

- `/posts/:id/loves`
	```
	method: POST
	example: /posts/612b7b3f1148ae87a61ab063/loves

	-----------
	loves/unloves the post with the specified id.
	-----------
	```

- `/posts/:id/loves/:username`
	```
	method: GET
	example: /posts/612b7b3f1148ae87a61ab063/loves/jeffalo

	-----------
	returns if a user has loved the post with the specified id.
	-----------
	```

- `/comments/:id`
	```
	method: GET
	example: /comments/60c4d33f1ea77fed94251ab7

	-----------
	returns the comment with the specified id.
	-----------

	method: DELETE
	example: /comments/60c4d33f1ea77fed94251ab7

	-----------
	deletes the comment with the specified id.
	-----------
	```

- `/posts`
	```
	method: POST
	body: {
		"post": "<p>hello world!</p>",
	}

	-----------
	creates a new post with the content specified in the "post" key within the request body.
	when creating a post, there are certain requirements that one must follow.

	requirements:
		- if your post contains any HTML elements, their tag must match one within
		the list of allowed tags below:
			- p
			- b
			- strong
			- i
			- em
			- u
			- s
			- li
			- ul
			- ol
			- mark
			- code
			- blockquote
			- pre
			- img

		any element that doesn't have a tag that matches one of these will simply be
		removed from the post.

		- any images in a post must have it's source come from one of the domains in
		the whitelist below:
			- wiki.wasteof.money
			- api.wasteof.money
			- u.cubeupload.com
			- i.ibb.co

	note: if you want to repost a post, you can add in the "repost" key with it's value being
	a post's id into your request's body.

	bug: having a mention be outside of a paragraph (p) element will NOT mention the user.
	```