# miscellaneous

- `/username-from-id/:id`

	![Does not require Authorization](https://img.shields.io/badge/requires_authorization-no-blue)
	```
	method: GET
	example: /username-from-id/60c4976b59c722b5661559c4

	-----------
		
	returns a user with the specified id.
	```

- `/username-available?username=:username`

	![Does not require Authorization](https://img.shields.io/badge/requires_authorization-no-blue)
	```
	method: GET
	example: /username-available?username=jeffalo

	-----------
		
	returns if a username is eligible for use or not.
	```

- `/random-post`

	![Does not require Authorization](https://img.shields.io/badge/requires_authorization-no-blue)
	```
	method: GET
	-----------
		
	returns a random post from the site.
