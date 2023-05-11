# messages

- `/messages/read`
	```
	method: GET
	-----------
	returns the currently logged in user's read messages.
	-----------
	```

- `/messages/unread`
	```
	method: GET
	-----------
	returns the currently logged in user's unread messages.
	-----------
	```

- `/messages/count`
	```
	method: GET
	-----------
	returns the currently logged in user's total message count.
	-----------
	```

- `/messages/mark/read`
	```
	method: POST
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
	body: {
		"messages": ["<message id>", "<message id>", ...]
	}
	
	-----------
	marks a message as unread.
	-----------
	```