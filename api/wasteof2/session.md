# session

- `/session`
	```
	method: GET
	-----------
	returns the currently logged in user's session.
	-----------
	
	method: POST
	-----------
	returns an authentication token depending on the values in the "username" and "password"
	keys in the request's body.
	-----------
	
	method: DELETE
	-----------
	logs you out of the currently logged in account.
	-----------
	```