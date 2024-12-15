# Summary

##  Extracting comment level
-   Only kept level 1. time complexity for level 2 and above is unknown as unimplemented.
##	Merging Submissions and Comments
-	Merged three submission DataFrames with their corresponding comments DataFrames using id (submissions) and link_id (comments).
-	Renamed all columns in comments with _comments suffix.
##	Filtering Comments by Time
-	Created function to retain only comments within 72 hours by default of post creation based on created_utc (post) and created_utc_comments (comment).
-	Resulted in filtered DataFrames aita_filtered, aio_filtered, ask_reddit_filtered.
##	Shape
-	printed shape
##  Save
-   Saved to `$bucket/project`


Filtered DataFrames Schema
```
root
 |-- id: string (nullable = true): The unique identifier for each submission post.
 |-- author: string (nullable = true): The username of the post’s author.
 |-- created_utc: long (nullable = true): The Unix timestamp of when the submission post was created.
 |-- subreddit: string (nullable = true): The subreddit to which the post was submitted.
 |-- title: string (nullable = true): The title of the submission post.
 |-- selftext: string (nullable = true): The body text of the submission post.
 |-- score: long (nullable = true): The score (upvotes - downvotes) of the submission post.
 |-- num_comments: long (nullable = true): The total number of comments on the submission post.
 |-- over_18: boolean (nullable = true): Indicates if the post is marked as NSFW.
 |-- created_date: string (nullable = true): The formatted date of when the post was created.
 |-- id_comments: string (nullable = true): The unique identifier for each comment.
 |-- author_comments: string (nullable = true): The username of the comment’s author.
 |-- link_id_comments: string (nullable = true): The ID of the submission post that this comment is associated with.
 |-- parent_id_comments: string (nullable = true): The ID of the parent comment or submission post that this comment is replying to.
 |-- created_utc_comments: long (nullable = true): The Unix timestamp of when the comment was created.
 |-- subreddit_comments: string (nullable = true): The subreddit in which the comment was posted.
 |-- body_comments: string (nullable = true): The content/body text of the comment.
 |-- score_comments: long (nullable = true): The score (upvotes - downvotes) of the comment.
 |-- gilded_comments: long (nullable = true): The count of times the comment was awarded Reddit "gold."
 |-- controversiality_comments: long (nullable = true): Indicates if the comment is considered controversial.
 |-- post_id_comments: string (nullable = true): A secondary identifier linking the comment to its post.
 |-- created_date_comments: string (nullable = true): The formatted date of when the comment was created.
 |-- comment_level_comments: integer (nullable = false): Indicates the level of the comment, where 1 signifies direct replies to the post. 1 only.

```
