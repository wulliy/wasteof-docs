# messages

- `/messages/read`

  	![Requires Authorization](https://img.shields.io/badge/requires_authorization-yes-blue)
	```
	method: GET
	headers:
		Authorization: "<token>"

	-----------
	returns the currently logged in user's read messages.
	-----------
	```

- `/messages/unread`

  	![Requires Authorization](https://img.shields.io/badge/requires_authorization-yes-blue)
	```
	method: GET
	headers:
		Authorization: "<token>"
	
	-----------
	returns the currently logged in user's unread messages.
	-----------
	```

- `/messages/count`

  	![Requires Authorization](https://img.shields.io/badge/requires_authorization-yes-blue)
	```
	method: GET
	headers:
		Authorization: "<token>"
	
	-----------
	returns the currently logged in user's total message count.
	-----------
	```

- `/messages/mark/read`

  	![Requires Authorization](https://img.shields.io/badge/requires_authorization-yes-blue)
	```
	method: POST
	headers:
		Authorization: "<token>"
	
	body: {
		"messages": ["<message id>", "<message id>", ...]
	}

	-----------	
	marks a message as read.
	-----------
	```

- `/messages/mark/unread`

	![Requires Authorization](https://img.shields.io/badge/requires_authorization-yes-blue)
	```
	method: POST
	headers:
		Authorization: "<token>"
	
	body: {
		"messages": ["<message id>", "<message id>", ...]
	}
	
	-----------
	marks a message as unread.
	-----------
	```
