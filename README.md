# ios-exercise

This is a small excercise to test ios/swift programming skills.

## Task

Develop a basic ios app using `XCode` with `Swift` implementing the following features:

1. Implement a view to display a list of `Post`s loaded from `/posts`
	- The posts must be displayed in a list
	- Each item in the list consists of an image, title and excerpt.
	- For the images placeholder images can be used but must not be hardcoded.  
2. Implement a detail view which displays the full post with a larger image when selected
3. Implement a comment section which accepts a `name`, `email` and `comment` as input and sends it to `/posts/{postId}/comments`
 	- The comment section must be prefilled with comments for this post retrieved over `/post/{id}/comments`
 	- Each comment entry must display the `name`, `email` and `comment`.
4. Provide proper user feedback for all interactions with the UI 


## API

The API can be found under `http://exercise.born-to-create.de/` and has the following routes:

### GET /posts

Retrieves a list of all posts

### GET /posts/{postId}/comments

Retrieve all comments for given posts

### POST /posts/{postId}/comments

Create a new comment

**Body**<br/>

`email`: string, required, valid email<br/>
`name`: string, required, allowed chars `a-z\s`, maxlength 100<br/>
`comment`: string, required, maxlength 300<br/>


## Entities

### Post

| Property | Type | Description |
| -------- | ---- | ----------- |
| id | int | |
| author | string | author full name |
| title | string | |
| thumbnail | string | thumbnail image url |
| image | string | full image url |
| content | string | |

### Comment

| Property | Type | Description |
| -------- | ---- | ----------- |
| id | int | |
| post_id | int | |
| name | string | comment author full name |
| email | string | author email address |
| comment | string | |

