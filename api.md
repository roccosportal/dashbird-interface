
## /api/posts/load/ ##
**Definition**

Will return an array of posts orderd by "updated" field. The user is wether the post owner or is in the share group.

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
					"created" : "(creation datetime)",
					"user" : "user@nest.com"
					}],
			"hash" : "(md5 post hash)"
		}]
	}

}
```

## /api/posts/get/ ##
**Definition**

Will return an array of posts by the given postIds. The user is wether the post owner or is in the share group.

**PARAMETERS(GET)**

Parameter | Example | Information
--- | --- | ---
postIds | ["(uuid)", "(uuid)"] | *(array of uuids)*
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
					"created" : "(creation datetime)",
					"user" : "user@nest.com"
					}],
			"hash" : "(md5 post hash)"
		}]
	}

}
```



## /api/posts/hashes/get/ ##
**Definition**

Will return an array of posts hashes orderd by "updated". The user is wether the post owner or is in the share group.

**PARAMETERS(GET)**

Parameter | Example | Information
--- | --- | ---
start-position | 0 | *(number)(optional)*
post-count | 50 | *(number)(optional)*
user-name | "user@nest.com" | *(text)(optional)(is required when you call the api from a different nest)*
user-token | "ad73jsad3" | *(text)(optional)(is required when you call the api from a different nest)*

**RESULT(json)**
```javascript
{	
	"STATUS":"STATUS_SUCCESS"
	"DATA" : {
		"posts": [{
			"postId" : "(uuid)",
			"hash" : "(md5 post hash)"
		}]
	}

}
```



## /api/post/get/ ##

**Definition**

Will return a post by the given postId. The user is wether the post owner or is in the share group.

**PARAMETERS(GET)**

Parameter | Example | Information
--- | --- | ---
postId | (uuid) | *(uuid)*
user-name | "user@nest.com" | *(text)(optional)(is required when you call the api from a different nest)*
user-token | "ad73jsad3" | *(text)(optional)(is required when you call the api from a different nest)*

**RESULT(json)**
```javascript
{	
	"STATUS":"STATUS_SUCCESS"
	"DATA" : {
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
				"created" : "(creation datetime)",
				"user" : "user@nest.com"
				}],
		"hash" : "(md5 post hash)"
	}

}
```


## /api/post/hash/get/ ##

**Definition**

Will return a post hash by the given postId. The user is wether the post owner or is in the share group.

**PARAMETERS(GET)**

Parameter | Example | Information
--- | --- | ---
postId | (uuid) | *(uuid)*
user-name | "user@nest.com" | *(text)(optional)(is required when you call the api from a different nest)*
user-token | "ad73jsad3" | *(text)(optional)(is required when you call the api from a different nest)*

**RESULT(json)**
```javascript
{	
	"STATUS":"STATUS_SUCCESS"
	"DATA" : {
			"postId" : "(uuid)",
			"hash" : "(md5 post hash)"
	}

}
```

## /api/post/comment/add/ ##

**Definition**

Will add a comment to a post by the given postId. The user is wether the post owner or is in the share group.

**PARAMETERS(GET)**

Parameter | Example | Information
--- | --- | ---
postId | (uuid) | *(uuid)*
text | "my new comment" | *(text)*
user-name | "user@nest.com" | *(text)(optional)(is required when you call the api from a different nest)*
user-token | "ad73jsad3" | *(text)(optional)(is required when you call the api from a different nest)*

**RESULT(json)**
```javascript
{	
	"STATUS":"STATUS_SUCCESS"
	"DATA" : {	
		"commentId" : "(uuid)",
		"text" : "(text)",
		"created" : "(creation datetime)",
		"user" : "user@nest.com"	
		}
	}

}
```


## /api/post/comment/delete/ ##

**Definition**

Will delete a comment to a post by the given commentId. The user is wether the comment owner.

**PARAMETERS(GET)**

Parameter | Example | Information
--- | --- | ---
commentId | (uuid) | *(uuid)*
user-name | "user@nest.com" | *(text)(optional)(is required when you call the api from a different nest)*
user-token | "ad73jsad3" | *(text)(optional)(is required when you call the api from a different nest)*

**RESULT(json)**
```javascript
{	
	"STATUS":"STATUS_SUCCESS"
}
```



