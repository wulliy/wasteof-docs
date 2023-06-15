# messages

- `/messages/read`
	```
	method: GET
	headers:
		Authorization: "<token>"

	-----------
	returns the currently logged in user's read messages.
	-----------
	```

- `/messages/unread`
	```
	method: GET
	headers:
		Authorization: "<token>"
	
	-----------
	returns the currently logged in user's unread messages.
	-----------
	```

- `/messages/count`
	```
	method: GET
	headers:
		Authorization: "<token>"
	
	-----------
	returns the currently logged in user's total message count.
	-----------
	```

- `/messages/mark/read`
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