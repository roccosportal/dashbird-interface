
## /api/posts/load/ ##
**Definition**

Will return an array of posts. The user is wether the post owner or is in the share group.

**PARAMETERS(GET)**


Parameter | Example | Information
--- | --- | ---
search | "text search" | *(text)(optional)*
start-position | 0 | *(number)(optional)*
post-count | 10 | *(number)(optional)*
user-name | "user@nest.com" | *(text)(optional)(is required when you call the api from a different nest)*
user-token | "ad73jsad3" | *(text)(optional)(is required when you call the api from a different nest)*


**RESULT(json)**
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
					"commentId" : "(uuid)",
					"text" : "(text)",
					"created" : "(creation datetime)"
					}]
		}]
	}

}
```

## /api/posts/get/ ##
**Definition**

Will return an array of posts by the given entryIds. The user is wether the post owner or is in the share group.


**PARAMETERS(GET)**

Parameter | Example | Information
--- | --- | ---
entryIds | ["(uuid)", "(uuid)"] | *(array of uuids)(required)*
user-name | "user@nest.com" | *(text)(optional)(is required when you call the api from a different nest)*
user-token | "ad73jsad3" | *(text)(optional)(is required when you call the api from a different nest)*

**RESULT(json)**

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
					"commentId" : "(uuid)",
					"text" : "(text)",
					"created" : "(creation datetime)"
					}]
		}]
	}

}
```



## /api/posts/hashes/get/ ##

## /api/post/get/ ##

## /api/post/hash/get/ ##

## /api/post/comment/add/ ##

## /api/post/comment/delete/ ##
