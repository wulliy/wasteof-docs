# settings

- `/settings`
	```
	method: GET
	headers:
		Authorization: "<token>"

	-----------
	i don't think you need a description to explain this one. it should be pretty self-explanatory.
	-----------
	```

- `/settings/auth/github`
	```
	method: DELETE
	headers:
		Authorization: "<token>"

	-----------
	deletes the Github authentication method, if one has been set.
	-----------
	```

- `/settings/auth/google`
	```
	method: DELETE
	headers:
		Authorization: "<token>"

	-----------
	deletes the Google authentication method, if one has been set.
	-----------
	```

- `/settings/auth/password`
	```
	method: DELETE
	headers:
		Authorization: "<token>"

	-----------
	deletes the password authentication method, if one has been set.
	not recommended that you do this.
	-----------

	method: PUT
	headers:
		Authorization: "<token>"

	-----------
	sets a new password for the currently logged in account.
	-----------
	```

- `/settings/auth/github/enable`
- `/settings/auth/github/disable`
	```
	method: POST
	headers:
		Authorization: "<token>"

	-----------
	enables / disables the Github authentication method.
	-----------
	```

- `/settings/auth/google/enable`
- `/settings/auth/google/disable`
	```
	method: POST
	headers:
		Authorization: "<token>"

	-----------
	enables / disables the Google authentication method.
	-----------
	```

- `/settings/auth/password/enable`
- `/settings/auth/password/disable`
	```
	method: POST
	headers:
		Authorization: "<token>"

	-----------
	enables / disables the password authentication method.
	not recommended that you disable this.
	-----------
	```

- `/settings/hide-recovery-message`
	```
	method: POST
	headers:
		Authorization: "<token>"

	-----------
	hides the alert about setting a recovery email so you can easily recover your
	account.
	-----------
	```

- `/settings/email`
	```
	method: DELETE
	headers:
		Authorization: "<token>"

	-----------
	deletes the recovery email set in the currently logged in account,
	if one has been set.
	-----------

	method: PUT
	headers:
		Authorization: "<token>"
		
	-----------
	sets a recovery email for the currently logged in account.
	if one has already been set, this will change it instead.
	-----------
	```

- `/settings/password-reset`
	```
	method: POST
	body: {
		"username": "jeffalo"
	}
	
	-----------
	sends an email to the recovery email set in the user with the specified
	username, if one has been sent.
	-----------
	```