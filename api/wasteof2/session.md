# session

- `/session`

	![Requires Authorization](https://img.shields.io/badge/requires_authorization-GET:_yes-blue)
	![Requires Authorization](https://img.shields.io/badge/requires_authorization-POST:_no-green)
	![Requires Authorization](https://img.shields.io/badge/requires_authorization-DELETE:_yes-orange)
	```
	method: GET
	headers:
		Authorization: "<token>"

	-----------
	returns the currently logged in user's session.
	-----------
	
	method: POST
	body: {
		"username": "<username>",
		"password": "<password>"
	}

	-----------
	returns an authentication token depending on the values in the "username" and "password"
	keys in the request's body.
	-----------
	
	method: DELETE
	headers:
		Authorization: "<token>"
	
	-----------
	logs you out of the currently logged in account.
	-----------
	```
