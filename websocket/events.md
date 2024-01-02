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
		- url: the url to redirect most clients to
	-----------
	redirect every web client currently online to a given URL, but only if it's been implemented.
	(note that for clients that don't make use of HTML or the web, this event may have to be
	 implemented in another way.)
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