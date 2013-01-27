## general ##

To make it possible multiple nests can communicate between each other this is a basic user authentication.



## workflow ##

user@nest1.com logs in into nest1.com. The server generates a user-token like "s3cr3t" and forwards it to the client.
The client calls nest2.com/api/posts/load/?user-name=user@nest1.com&user-token=s3cr3t. The server nest2.com calls nest1.com/api/user/authenticate?user-name=user@nest1.com&user-token=s3cr3t. nest1.com answers that this token is associated to the user. nest2.com delievers the requested posts.

## flowchart ##


client	| nest1.com | nest2.com
user@nest1.com log in to nest1.com | (generating secret) | (nothing)
/api/posts/load/?user-name=user@nest1.com&user-token=s3cr3t | (nothing) | (recieving request)
(waiting)| (recieving request) | nest1.com/api/user/authenticate?user-name=user@nest1.com&user-token=s3cr3t
(waiting)| is authenticated | (recieving result)
(recieving result)| (nothing) | send posts
