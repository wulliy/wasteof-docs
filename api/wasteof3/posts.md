# posts

- `/posts/:id:/__data.json`
	```
	method: GET
	-----------
	returns the post with the specified id.
	-----------
	```

- `/posts/:id/reposts/__data.json`
	```
	method: GET
	-----------
	returns a list of all the posts that reposted the post with the specified
	id.
	-----------
	```

- `/posts/:id/comments/:id/__data.json`
	```
	method: GET
	-----------
	returns a comment with the specified comment id under a post with the specified post
	id.
	-----------
	```

- `/posts/:id/loved`
	```
	method: GET
	-----------
	returns if the currently logged in account has loved the post with the specified
	id or not.
	-----------

	method: POST
	-----------
	loves/unloves a post with the specified id.
	-----------
	```

- `/posts/:id/comments`
	```
	method: POST
	body: {
		"content": "<p>comment</p>"
	}

	-----------
	creates a comment under the post with the specified id.
	-----------
	```

- `/posts/:id/comments/:id/replies`
	```
	method: POST
	body: {
		"content": "<p>reply</p>"
	}

	-----------
	replies to a comment with the specified comment id under the post with the
	specified post id.
	-----------
	```

- `/comments/:id`
	```
	method: DELETE
	-----------
	deletes a comment/reply with the specified comment id.
	-----------
	```

- `/posts`
	```
	the same specification as the wasteof2 /posts endpoint.
	```