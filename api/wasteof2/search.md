# search

- `/search/users`

  	![Requires Authorization](https://img.shields.io/badge/requires_authorization-no-blue)
	```
	method: GET
	example: /search/users?q=jeffalo

	-----------
	returns an amount of users depending on the query provided through the "?q" URL
	parameter.

	an additional "?page" URL parameter can be added to specify the page that will be
	returned.
	-----------
	```

- `/search/posts`

	![Requires Authorization](https://img.shields.io/badge/requires_authorization-yes-blue)
	```
	method: GET
	example: /search/posts?q=site&page=2
	
	-----------
	returns an amount of posts depending on the query provided through with "?q" URL
	parameter.

	an additional "?page" URL parameter can be added to specify the page that will be
	returned.
	-----------
	```
