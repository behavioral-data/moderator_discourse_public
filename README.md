# Perceptions of Moderators as a Large-Scale Measure of Online Community Governance

This website is a companion site for our paper titled Perceptions of Moderators as a Large-Scale Measure of Online Community Governance. A preprint of this paper is available on [arXiv](https://arxiv.org/abs/2401.16610), please read it for more details on our methods and results.

A summary of our results and some additional discussion is available over at [/r/TheoryOfReddit](https://www.reddit.com/r/TheoryOfReddit/comments/1ary8x8/identifying_promising_moderation_strategies/).

# Moderator Discourse Data

We are in the process of computing moderator discourse data for a larger time period. For now, data is available for all subreddits from January 2020-June 2021, the same time period covered in our paper. Due to reddit licensing issues, we only make 'dehydrated' data available here, which is to say we do not include the content of the posts and comments, only their sentiment with regards to moderators, along with some metadata for convenience. If you have any questions, please contact Galen Weld, the corresponding author for this work.

## Data Schema

The data consists of the following fields, in `.csv` format:
- `id`: the post or comment id
- `subreddit`: the subreddit the post or comment was in
- `kind`: post or comment
- `timestamp`: timestamp the post or comment was created, in seconds since the unix epoch (UTC)
- `sentiment_wrt_mods`: the sentiment predicted our by our model: positive, neutral, or negative

## Data Files
2020-01.jsonl: 11,175 posts, 106,488 comments
2020-02.jsonl: 10,331 posts, 95,337 comments
2020-03.jsonl: 11,599 posts, 91,881 comments
2020-04.jsonl: 11,571 posts, 88,047 comments
2020-05.jsonl: 14,558 posts, 105,927 comments
2020-06.jsonl: 13,941 posts, 116,752 comments
2020-07.jsonl: 13,187 posts, 106,283 comments
2020-08.jsonl: 15,821 posts, 125,424 comments
2020-09.jsonl: 9,243 posts, 90,987 comments
2020-10.jsonl: 8,527 posts, 92,199 comments
2020-11.jsonl: 8,673 posts, 77,257 comments
2020-12.jsonl: 7,735 posts, 81,593 comments
2021-01.jsonl: 11,034 posts, 108,171 comments
2021-02.jsonl: 10,734 posts, 89,859 comments
2021-03.jsonl: 10,417 posts, 100,067 comments
2021-04.jsonl: 9,932 posts, 99,853 comments
2021-05.jsonl: 9,366 posts, 53,498 comments
2021-06.jsonl: 8,387 posts, 64,928 comments
