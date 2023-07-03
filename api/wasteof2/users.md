# users

- `/users`
	```
	method: POST
	body: {
		"username": "jeffalo",
		"password": "a"
	}
	
	-----------
	creates a new account depending on the request's body.
	-----------
	```

- `/users/:username`
	```
	method: GET
	example: /users/jeffalo

	-----------
	returns the profile of a user.
	-----------
	```

- `/users/:username/followers`
	```
	method: GET
	example: /users/jeffalo/followers

	-----------
	returns the users that are currently following a user.
	-----------

	method: POST
	headers:
		Authorization: "<token>"

	example: /users/jeffalo/followers
	
	-----------
	follows / unfollows a user.
	-----------
	```

- `/users/:username/following`
	```
	method: GET
	example: /users/jeffalo/following

	-----------
	returns the users that a user is following.
	-----------
	```

- `/users/:username/following/posts`
	```
	method: GET
	example: /users/jeffalo/following/posts

	-----------
	return a user's feed
	-----------
	```

- `/users/:username/posts`
	```
	method: GET
	example: /users/jeffalo/posts?page=2

	-----------
	return a user's posts.

	an additional "?page" URL parameter can be added to specify which page should be
	returned.
	-----------
	```

- `/users/:username/name`
	```
	method: GET
	example: /users/jeffalo/name

	-----------
	return a user's username.
	-----------

	method: PUT
	headers:
		Authorization: "<token>"

	example: /users/jeffalo/name

	-----------
	changes a user's name, if the new username is available.
	-----------
	```

- `/users/:username/bio`
	```
	method: PUT
	headers:
		Authorization: "<token>"

	body: {
		"content": "new bio"
	}

	example: /users/jeffalo/bio

	-----------
	changes a user's bio.
	-----------
	```

- `/users/:username/picture`
	```
	method: GET
	example: /users/jeffalo/picture?optimized=true

	-----------
	returns a user's profile picture as either an image or an SVG.
	if no user with the specified username exists, it'll return an automatically generated SVG
	instead.

	an additional "?optimized" URL parameter can be added to get an optimized equivalent.
	-----------

	method: PUT
	headers:
		Authorization: "<token>"

	example: /users/jeffalo/picture

	-----------
	changes a user's profile picture. this must be an valid image.
	note: any animated images will be automatically converted into static PNGs.
	-----------
	```

- `/users/:username/banner`
	```
	method: GET
	example: /users/jeffalo/banner?optimized=true

	-----------
	returns a user's banner as an image.
	if no user with the specified username exists, it won't return anything.

	an additional "?optimized" URL parameter can be added to get an optimized equivalent.
	-----------

	method: PUT
	headers:
		Authorization: "<token>"

	example: /users/jeffalo/banner

	-----------
	changes a user's banner. this must be an valid image.
	note: any animated images will be automatically converted into static PNGs.
	-----------
	```

- `/users/:username/surprise`
	```
	method: POST
	headers:
		Authorization: "<token>"
	
	example: /users/jeffalo/surprise

	-----------
	sets a random color for your profile.
	the available colors you can get are:
		- "red"
		- "orange"
		- "yellow"
		- "green"
		- "teal"
		- "blue"
		- "indigo"
		- "fuchsia"
		- "pink"
		- "gray"

	the ratelimit for this endpoint is an hour
	(note: you can only do this 5 times before you run out of surprises)
	-----------
	```