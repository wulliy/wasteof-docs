# search

- `/search/users`
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