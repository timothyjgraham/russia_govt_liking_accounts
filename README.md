# Pro-Russian 'liking' accounts on Twitter

Account IDs and instructions for how to reproduce [my analysis of Twitter accounts](https://www.abc.net.au/news/science/2022-03-30/ukraine-war-twitter-bot-network-amplifies-russian-disinformation/100944970) that liked tweets from Russian government and embassy accounts.

## Step 1

The IDs of all accounts are provided in the repository as a text file: `liking_ALL_users_account_IDs.txt`.

You can use this text file to collect all the account information via the Twitter API. Personally I use the [twarc2 software](https://twarc-project.readthedocs.io/en/latest/twarc2_en_us/) and the following command to collect user information for a set of IDs:

```
twarc2 users liking_ALL_users_account_IDs.txt liking_ALL_users_account_IDs.jsonl
```

## Step 2

For the [bot analysis](https://twitter.com/timothyjgraham/status/1508029324334870528) I used the [Botometer model via the API](https://rapidapi.com/OSoMe/api/botometer-pro).

Specifically, I ran Botometer on 16513 accounts in the dataset that were created in 2022. The 'free' plan has a rate limit of checking 2000 accounts per day and there is a hard limit of 17,280 accounts per day which is due to the rate limits of the Twitter API itself. Therefore, I focussed attention on the most recently created accounts, many of which were created on the day Russia invaded Ukraine (24th February 2022).

You will need to run Botometer on the account IDs provided in Step 1, or a subset (e.g. accounts created in 2022). I did this in Python but it is possible to do it using other methods too, and [Botometer provides instructions](https://rapidapi.com/OSoMe/api/botometer-pro/details) for how to run the model.

