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
		- url: the url to redirect everyone to
	-----------
	redirects every user currently online to the URL specified within the event.

	(note: this only works if your client supports this event, otherwise it won't redirect)
	-----------
	```

- `message`
	```
	arguments:
		- content: the content that your message will contain
	-----------
	sends a messsage with the specified content into the public chat. (/chat)
	-----------
	```