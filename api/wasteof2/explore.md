# explore

- `/explore/users/top`
	```
	method: GET
	-----------
	returns the top followed users on the explore page.
	-----------
	```
 
	<details>
		<summary>Reponse schema:</summary>

		[
		    {
			"name":"jeffalo",
			"id":"60c4976b59c722b5661559c4",
			"bio":"creator of wasteof.money (very cool) (my real name isn't actually jeffalo)",
			"verified":true,
			"permissions": {
				"admin":true,
				"banned":false
			},
			"beta":true,
			"color":"yellow",
			"links":[],
			"history":{
				"joined":1623496555000
			},
			"stats":{"followers":702}
		    }
		]
  
	</details>
 	

- `/explore/posts/trending`
	```
	method: GET
	example: /explore/posts/trending?timeframe=week
	
	-----------
	returns the posts that are currently trending.

	an additional "?timeframe" URL parameter can be added to only fetch the posts that
	were trending during that time frame.

	the supported values for this parameter are:
	- "day"
	- "week"
	- "month"
	- "all"
	-----------
	```
