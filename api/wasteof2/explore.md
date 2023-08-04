# explore

- `/explore/users/top`

	![Does not require Authorization](https://img.shields.io/badge/requires_authorization-no-blue)
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
			"links":[
  				    {
  					"label":"jeffalo.net ",
  					"url":"https://jeffalo.net"
  				    }
  			],
			"history":{
				"joined":1623496555000
			},
			"stats":{
  				"followers":702
  			}
		    }
		]
  
	</details>
 	

- `/explore/posts/trending`

	![Does not require Authorization](https://img.shields.io/badge/requires_authorization-no-blue)
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

	 <details>
		<summary>Reponse schema:</summary>
		 
		{
  			"posts": [
  			    {
  				"_id": "64aa9e57370c70051d4843e3",
				"poster": {
  					"name": "wuilly",
  					"id": "60c4b7db3db707d5ec773b40",
					"color": "yellow"
				},
  				"content": "<p>please take good care of my rabbit his name is shawn and this is what he looks like</p><p>thank you</p><img src=\"https://u.cubeupload.com/8ed/wabbit.png\">",
				"time": 1688903255536,
				"__order": 1,
				"revisions": [
  				    {
					"content": "<p>please take good care of my rabbit his name is shawn and this is what he looks like</p><p>thank you</p><img src=\"https://u.cubeupload.com/8ed/wabbit.png\">",
  					"time": 1688903255536,
  					"current": true
				    }
  				],
				"comments": 9,
				"loves": 18,
				"reposts": 1
		 	    },
  			],
  			"since": "week"
		}
  
	</details>

 
