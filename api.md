
## /api/posts/load/ ##

_PARAMETERS(GET)_
search="text search"_(text)__(optional)_
start-position=0_(number)__(optional)_
post-count=10_(number)__(optional)_
user-token=_(number)__(optional)__(is required when you call the api from a different nest)_

_RESULT(json)_
 ```javascript
{	
	"STATUS":"STATUS_SUCCESS"
	"DATA" : {
		"posts": [{
			"postId" : "(uuid)",
			"created" : "(creation datetime)",
			"updated" : "(updated datetime)",
			"text" : "(text)",
			"tags" : ["tag1", "tag2"],
			"user" : "user@nest.com",
			"shares": ["user2@nest.com", "user3@nest.org"],
			"comments" : [{
					commentId : "(uuid)",
					text : "(text)",
					"created" : "(creation datetime)"
					}]
		}]
	}

}
```

## /api/posts/get/ ##

## /api/posts/hashes/get/ ##

## /api/post/get/ ##

## /api/post/hash/get/ ##

## /api/post/comment/add/ ##

## /api/post/comment/delete/ ##
