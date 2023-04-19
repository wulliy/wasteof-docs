# users

- `/users`
	```
	method: GET
	-----------
	returns the amount of registered accounts on the site.
	-----------
	```

- `/users/:name/__data.json`
	```
	method: GET
	-----------
	returns a profile of the user with the specified name.
	-----------
	```

- `/users/:name/picture`
	```
	method: GET
	-----------
	redirects to the api.wasteof.money equivalent.
	-----------
	```

- `/users/:name/banner`
	```
	method: GET
	-----------
	redirects to the api.wasteof.money equivalent.
	-----------
	```

- `/users/:name/sidebar`
	```
	method: PUT
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
	```
	method: POST
	body: {
		"color": "yellow"
	}

	-----------
	sets the profile color of the user with the specified name to the one
	in the request's body.
	-----------
	```