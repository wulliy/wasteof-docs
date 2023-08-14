# posts

- `/posts/:id:/__data.json`

	![Requires Authorization](https://img.shields.io/badge/requires_authorization-no-blue)
	```
	method: GET
	-----------
	returns the post with the specified id.
	-----------
	```

- `/posts/:id/reposts/__data.json`

	![Requires Authorization](https://img.shields.io/badge/requires_authorization-no-blue)
	```
	method: GET
	-----------
	returns a list of all the posts that reposted the post with the specified
	id.
	-----------
	```

- `/posts/:id/comments/:id/__data.json`

	![Requires Authorization](https://img.shields.io/badge/requires_authorization-no-blue)
	```
	method: GET
	-----------
	returns a comment with the specified comment id under a post with the specified post
	id.
	-----------
	```

- `/posts/:id/loved`

	![Requires Authorization](https://img.shields.io/badge/requires_authorization:_GET-no-blue)
	![Requires Authorization](https://img.shields.io/badge/requires_authorization:_POST-yes-blue)
	```
	method: GET
	-----------
	returns if the currently logged in account has loved the post with the specified
	id or not.
	-----------

	method: POST
 	headers:
 		Authorization: "<token>"
	-----------
	loves/unloves a post with the specified id.
	-----------
	```

- `/posts/:id/comments`

	![Requires Authorization](https://img.shields.io/badge/requires_authorization-yes-blue)
	```
	method: POST
 	headers:
 		Authorization: "<token>"
	body: {
		"content": "<p>comment</p>"
	}

	-----------
	creates a comment under the post with the specified id.
	-----------
	```

- `/posts/:id/comments/:id/replies`

	![Requires Authorization](https://img.shields.io/badge/requires_authorization-yes-blue)
	```
	method: POST
 	headers:
	 	Authorization: "<token>"
	body: {
		"content": "<p>reply</p>"
	}

	-----------
	replies to a comment with the specified comment id under the post with the
	specified post id.
	-----------
	```

- `/comments/:id`

  	![Requires Authorization](https://img.shields.io/badge/requires_authorization-yes-blue)
	```
	method: DELETE
	-----------
	deletes a comment/reply with the specified comment id.
	-----------
	```

- `/posts`

	![Requires Authorization](https://img.shields.io/badge/requires_authorization-see_wasteof2_docs-black)
	```
	the same specification as the wasteof2 /posts endpoint.
	```
