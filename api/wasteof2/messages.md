# messages

- `/messages/read`

  	![Requires Authorization](https://img.shields.io/badge/requires_authorization-yes-blue)
	```
	method: GET
	headers:
		Authorization: "<token>"

	-----------
	returns the currently logged in user's read messages.
	-----------
	```

 	<details>
		<summary>Reponse schema:</summary>

		{
  		  "read": [
        		{
            		  "_id": "64cd0f5fc2d93c04fd6baba3",
  				  "type": "comment_reply",
            		  "to": {
                	  	"name": "imadeanaccount",
                	  	"id": "63fcf11ebac4b7a8034e1327"
  			  	  },
  				  "data": {
  				    "actor": {
                    			"name": "wasteofplus",
                    			"id": "64a834d75f4b2a0db409bc3e"
                		    },
  				    "post": {
  					"_id": "64cd07f7c2d93c04fd6bab8a",
                    			"poster": {
  					    "name": "micahlt",
  					    "id": "623f913c09dd2804f2c00e94",
  					    "color": "indigo"
                    			},
                    	  		"content": "<p>me when birth</p>",
                    			"time": 1691158519007,
                    			"revisions": [
  						{
                            		  	  "content": "<p>me when birth</p>",
                            		  	  "time": 1691158519007,
                            		  	  "current": true
                        			}
                   		 	],
                    			"comments": 8,
                    			"loves": 7,
                    			"reposts": 0
  				    },
                		    "comment": null
  			  	  },
            			  "read": true,
            			  "time": 1691160415432
  		        },
  		   ]
                }
  
	</details>

- `/messages/unread`

  	![Requires Authorization](https://img.shields.io/badge/requires_authorization-yes-blue)
	```
	method: GET
	headers:
		Authorization: "<token>"
	
	-----------
	returns the currently logged in user's unread messages.
	-----------
	```

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

- `/messages/mark/read`

  	![Requires Authorization](https://img.shields.io/badge/requires_authorization-yes-blue)
	```
	method: POST
	headers:
		Authorization: "<token>"
	
	body: {
		"messages": ["<message id>", "<message id>", ...]
	}

	-----------	
	marks a message as read.
	-----------
	```

- `/messages/mark/unread`

	![Requires Authorization](https://img.shields.io/badge/requires_authorization-yes-blue)
	```
	method: POST
	headers:
		Authorization: "<token>"
	
	body: {
		"messages": ["<message id>", "<message id>", ...]
	}
	
	-----------
	marks a message as unread.
	-----------
	```
