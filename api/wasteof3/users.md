# users

- `/users`

	![Requires Authorization](https://img.shields.io/badge/requires_authorization-no-blue)
	```
 	method: GET
	-----------
	returns the amount of registered accounts on the site.
	-----------
	```

- `/users/:name/__data.json`

	![Requires Authorization](https://img.shields.io/badge/requires_authorization-no-blue)
	```
	method: GET
	-----------
	returns a profile of the user with the specified name.
	-----------
	```

- `/users/:name/picture`

	![Requires Authorization](https://img.shields.io/badge/requires_authorization-no-blue)
	```
	method: GET
	-----------
	redirects to the api.wasteof.money equivalent.
	-----------
	```

- `/users/:name/banner`

	![Requires Authorization](https://img.shields.io/badge/requires_authorization-no-blue)
	```
	method: GET
	-----------
	redirects to the api.wasteof.money equivalent.
	-----------
	```

- `/users/:name/sidebar`

	![Requires Authorization](https://img.shields.io/badge/requires_authorization:_PUT-yes-green)
	```
	method: PUT
 	headers:
 		Authorization: "<token>"
	body: {
		"sidebar": [
			{
				"type": "TextBlock",
				"data": {
					"title": "i am a title",
					"text": "and i am text"
				}
			}
		]
	}

	-----------
	sets the sidebar of the user with the specified name to the JSON in
	the request's body.
	-----------
	```

- `/users/:name/color`

	![Requires Authorization](https://img.shields.io/badge/requires_authorization-yes-blue)
	```
	method: POST
 	headers:
 		Authorization: "<token>"
	body: {
		"color": "yellow"
	}

	-----------
	sets the profile color of the user with the specified name to the one
	in the request's body.
	-----------
	```
