## High level overview

1. post questions to the public
2. comments on existing post/questions
3. upvote/ downvote/ comments
4. feed of most popular posts

### Design problem - solution steps

1. gathering functional and non functional requirements
2. defining the system api
3. architectural diagrams -Addressing functional requirements
4. architectural diagrams -Addressing non functional requirements

### System design - initial questions 1. gathering requirements

1. can anyone post or view post/questions
2. what can a post contain?(text/image/video)
3. whats the meaning of popular posts
4. what is the structure of flat list vs tree

### functional requirements

1. A user can sign up and login to post, vote or comment.
2. A user should be able to create a new post that contains a title,topic tags,body.
3. A user should be able to comment on any existing post.
4. comments are ordered chronologically as flat list.
5. user can delete their own post or comment
6. logged in user can upvote /downvote an existing post/comment
7. present the top most popular posts in the last 24 hours on the home page(popularity = upvotes-downvotes)

### non functional requirements

1. scalability(millions of users)
2. performance(less than 500ms response time )
3. fault tolerance/ high availability(99.9%)
4. availability
5. durability(post / comments should not disappear, should be always present)

### System design - 2. defining system api

1. identify entities(users,posts,comments,images,votes)
2. mapping entities to URIs(/users,/users/{user-id},/posts,/posts/{post-id},/post/{post-id}/comments,/post/{post-id}/comments/{comment-id})
3. defining resources representations
4. assigning http methods to operations on resources
