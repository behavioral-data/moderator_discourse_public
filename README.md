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

We are in the process of computing moderator discourse data for a larger time period. For now, data is available for all subreddits from April 2017-May 2022, which is several more years than the time period covered in our paper. Due to reddit licensing issues, we only make 'dehydrated' data available here, which is to say we do not include the content of the posts and comments, only their sentiment with regards to moderators, along with some metadata for convenience. If you have any questions, or would like help hydrating the data, please contact Galen Weld, the corresponding author for this work.

## Data Schema

The data consists of the following fields, in `.csv` format:
- `id`: the post or comment id
- `subreddit`: the subreddit the post or comment was in
- `kind`: post or comment
- `timestamp`: timestamp the post or comment was created, in seconds since the unix epoch (UTC)
- `sentiment_wrt_mods`: the sentiment predicted our by our model: positive, neutral, or negative

There are two files per month. `RS_YYYY-MM.csv` includes submissions (posts) for that month, and `RC_YYYY-MM.csv` includes comments.

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

