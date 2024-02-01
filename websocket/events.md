# events

- `updateMessageCount`
	```
	arguments:
		- message: the amount of messages
	-----------
	updates the current message count.
	-----------
	```

- `redirect`
	```
	arguments:
		- url:  the url to redirect most clients to
		- user: if specified, the user to redirect
	-----------
	redirect either everyone, or one user to a given URL via the client, but only if it's been implemented.
	this event may only be emitted if the sender is an admin.

	(note that for clients that don't make use of HTML or any web technologies, this event may be implemented
	 another way, or not be implemented at all.)
	-----------
	```

- `message`
	```
	arguments:
		- content: the content that your message will contain
	-----------
	sends a messsage with some content into the public chat. (/chat)
	-----------
	```