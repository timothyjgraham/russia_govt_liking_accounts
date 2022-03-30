# Pro-Russian liking accounts on Twitter

Account IDs and instructions for how to reproduce [my analysis of Twitter accounts](https://www.abc.net.au/news/science/2022-03-30/ukraine-war-twitter-bot-network-amplifies-russian-disinformation/100944970) that liked tweets from Russian government and embassy accounts.

## Step 1

The IDs of all accounts are provided in the repository as a text file: `liking_ALL_users_account_IDs.txt`.

You can use this text file to collect all the account information via the Twitter API. Personally I use the [twarc2 software](https://twarc-project.readthedocs.io/en/latest/twarc2_en_us/) and the following command to collect user information for a set of IDs:

```
twarc2 users liking_ALL_users_account_IDs.txt liking_ALL_users_account_IDs.jsonl
```

