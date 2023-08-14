# session

- `/login`

	![Requires Authorization](https://img.shields.io/badge/requires_authorization-no-blue)
	```
	method: POST
	body: {
		"username": "jeffalo",
		"password": "a"
	}

	-----------
	returns an authentication token depending on the specified "username" and "password" values in the
	request's body.
	-----------
	```
