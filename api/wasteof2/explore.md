# explore

- `/explore/users/top`
	```
	method: GET
	-----------
	returns the top followed users on the explore page.
	-----------
	```

- `/explore/posts/trending`
	```
	method: GET
	example: /explore/posts/trending?timeframe=week
	
	-----------
	returns the posts that are currently trending.

	an additional "?timeframe" URL parameter can be added to only fetch the posts that
	were trending during that time frame.

	the supported values for this parameter are:
	- "week"
	- "month"
	- "all"
	-----------
	```