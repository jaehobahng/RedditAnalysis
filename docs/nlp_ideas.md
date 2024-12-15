# NLP Ideas

Dataset Schema

3 merged datasets
```
root
 |-- post_id: string (nullable = true)
 |-- post_author: string (nullable = true)
 |-- created_utc_post: long (nullable = true)
 |-- subreddit_post: string (nullable = true)
 |-- post_title: string (nullable = true)
 |-- selftext: string (nullable = true)
 |-- score_post: long (nullable = true)
 |-- num_comments: long (nullable = true)
 |-- over_18: boolean (nullable = true)
 |-- created_date_post: string (nullable = true)
 |-- comment_id: string (nullable = true)
 |-- comment_author: string (nullable = true)
 |-- link_id: string (nullable = true)
 |-- parent_id: string (nullable = true)
 |-- created_utc_comment: long (nullable = true)
 |-- subreddit_comment: string (nullable = true)
 |-- comment_body: string (nullable = true)
 |-- score_comment: long (nullable = true)
 |-- gilded: long (nullable = true)
 |-- controversiality: long (nullable = true)
 |-- top_level_comment: integer (nullable = true)
 |-- created_date_comment: string (nullable = true)
 |-- time_since_post: double (nullable = true)

```

posts
```
root
 |-- post_id: string (nullable = true)
 |-- post_author: string (nullable = true)
 |-- created_utc_post: long (nullable = true)
 |-- subreddit_post: string (nullable = true)
 |-- post_title: string (nullable = true)
 |-- selftext: string (nullable = true)
 |-- score_post: long (nullable = true)
 |-- num_comments: long (nullable = true)
 |-- over_18: boolean (nullable = true)
 |-- created_date_post: string (nullable = true)
 |-- sentiment_score: long (nullable = true)
 |-- overall_sentiment: string (nullable = true)
 |-- top_words_tfidf: string (nullable = true) <Dictionary> {word(string): tfidf(long)}
```

## Visualization

- What would be the sentiment score difference between nsfw submissions and non nsfw submissions?
- Top words score distribution plot
- Sentiment score distribution difference in a year across subreddits
- regex grepping for YTA/NTA/ESH/NAH/INFO 

## Summary Stats
- constant over the months
- sentiment score variance/std, mean, quantiles

> [!INFO]
> sentiment score can be calculated for both submission and comments. currently only
> submission is calculated. Would it be necessary to calculate for comments? if so,
> what would be the question?
