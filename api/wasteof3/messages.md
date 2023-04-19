# messages

- `/messages/count`
	```
	method: GET
	-----------
	returns the currently logged in user's total message count.
	-----------
	```

- `/messages/__data.json`
	```
	method: GET
	example: /messages/__data.json?page=2
	
	-----------
	returns all of the currently logged in user's messages.

	an additional "?page" URL parameter can be added to get a specific page of messages.
	-----------
	```

- `/messages/mark-all-as-read`
	```
	method: POST
	-----------
	marks all of the currently logged in user's messages to be read.
	-----------
	```