# Perceptions of Moderators as a Large-Scale Measure of Online Community Governance

This website is a companion site for our paper titled Perceptions of Moderators as a Large-Scale Measure of Online Community Governance, which will appear at CSCW 2025. A preprint of this paper is available on [arXiv](https://arxiv.org/abs/2401.16610), please read it for more details on our methods and results.

A summary of our results and some additional discussion is available over at [/r/TheoryOfReddit](https://www.reddit.com/r/TheoryOfReddit/comments/1ary8x8/identifying_promising_moderation_strategies/).

If you make use of our data, please cite our paper:
```
@misc{weld2024perceptions,
      title={Perceptions of Moderators as a Large-Scale Measure of Online Community Governance}, 
      author={Galen Weld and Leon Leibmann and Amy X. Zhang and Tim Althoff},
      year={2025},
      journal={CSCW},
}
```

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

| Filename      | Number of Posts | Number of Comments | Total Records |
|---------------|-----------------|--------------------|---------------|
| 2020-01.jsonl | 11,175 posts    | 106,488 comments   | 117,663 total |
| 2020-02.jsonl | 10,331 posts    | 95,337 comments    | 105,668 total |
| 2020-03.jsonl | 11,599 posts    | 91,881 comments    | 103,480 total |
| 2020-04.jsonl | 11,571 posts    | 88,047 comments    | 99,618 total  |
| 2020-05.jsonl | 14,558 posts    | 105,927 comments   | 120,485 total |
| 2020-06.jsonl | 13,941 posts    | 116,752 comments   | 130,693 total |
| 2020-07.jsonl | 13,187 posts    | 106,283 comments   | 119,470 total |
| 2020-08.jsonl | 15,821 posts    | 125,424 comments   | 141,245 total |
| 2020-09.jsonl | 9,243 posts     | 90,987 comments    | 100,230 total |
| 2020-10.jsonl | 8,527 posts     | 92,199 comments    | 100,726 total |
| 2020-11.jsonl | 8,673 posts     | 77,257 comments    | 85,930 total  |
| 2020-12.jsonl | 7,735 posts     | 81,593 comments    | 89,328 total  |
| 2021-01.jsonl | 11,034 posts    | 108,171 comments   | 119,205 total |
| 2021-02.jsonl | 10,734 posts    | 89,859 comments    | 100,593 total |
| 2021-03.jsonl | 10,417 posts    | 100,067 comments   | 110,484 total |
| 2021-04.jsonl | 9,932 posts     | 99,853 comments    | 109,785 total |
| 2021-05.jsonl | 9,366 posts     | 53,498 comments    | 62,864 total  |
| 2021-06.jsonl | 8,387 posts     | 64,928 comments    | 73,315 total  |

## Data Download
You may download all the above files, or individual files, from our [github repo](https://github.com/behavioral-data/moderator_discourse_public).


## Daily Counts Data
If you prefer, we also provide a single large `.csv` containing daily counts, for each subreddit, of the number of posts and comments with positive, neutral, and negative sentiment with regards to the moderators. Importantly, these data also include counts of total posts and comments (of any type, not just those addressing moderators), as well as the number of removed and deleted comments (detected using [removed] tags). You may download this file [here](https://drive.google.com/file/d/14J-jmKaq3HSn7gkL6duhYUWMu8QOOT-0/view?usp=sharing). It spans from July 2018 to June 2021.

The data consists of the following columns:
- `subreddit`: the name of the subreddit
- `date`: the date of the count (UTC time delineated)
- `total_posts`: total number of posts, of any type
- `total_comments`: total number of comments, of any type
- `removed_comments`: total number of posts that were removed by moderators
- `removed_posts`: total number of comments that were removed by moderators
- `mod_items_positive`: total number of posts and comments discussing moderators, and expressing positive sentiment towards those moderators
- `mod_items_negative`: total number of posts and comments discussing moderators, and expressing negative sentiment towards those moderators
- `mod_items_neutral`: total number of posts and comments discussing moderators, and expressing neutral sentiment towards those moderators

