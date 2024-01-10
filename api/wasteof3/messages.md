# messages

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

- `/messages/__data.json`

 	![Requires Authorization](https://img.shields.io/badge/requires_authorization-yes-blue)
	```
	method: GET
 	headers:
 		Authorization: "<token>"
	example: /messages/__data.json?page=2
	
	-----------
	returns all of the currently logged in user's messages.

	an additional "?page" URL parameter can be added to get a specific page of messages.
	-----------
	```

- `/messages/mark-all-as-read`

 	![Requires Authorization](https://img.shields.io/badge/requires_authorization-yes-blue)
	```
	method: POST
  	headers:
 		Authorization: "<token>"
	-----------
	marks all of the currently logged in user's messages to be read.
	-----------
	```
