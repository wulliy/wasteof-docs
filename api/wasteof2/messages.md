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
	-----------	
	marks a message as read.
	-----------
	```

- `/messages/mark/unread`
	```
	method: POST
	-----------
	marks a message as unread.
	-----------
	```