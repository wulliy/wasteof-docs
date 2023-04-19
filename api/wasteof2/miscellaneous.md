# miscellaneous

- `/username-from-id/:id`
	```
	method: GET
	example: /username-from-id/60c4976b59c722b5661559c4

	-----------
		
	returns a user with the specified id.
	```

- `/username-available?username=:username`
	```
	method: GET
	example: /username-available?username=jeffalo

	-----------
		
	returns if a username is eligible for use or not.
	```

- `/random-post`
	```
	method: GET
	-----------
		
	returns a random post from the site.