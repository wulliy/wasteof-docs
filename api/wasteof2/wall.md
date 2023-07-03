# wall

- `/users/:username/wall`
	```
	method: GET
	-----------
	returns the comments of the user's wall with the specified username.

	an additional "?page" URL parameter can be added to return the comments on a
	wall from a specified page.
	-----------
	
	method: POST
	headers:
		Authorization: "<token>"
	
	body: {
		"content": "wall content"
	}
	
	-----------
	creates a comment or reply on a user's wall with the specified username depending
	on if the "?parent" URL parameter is specified.
	-----------
	```