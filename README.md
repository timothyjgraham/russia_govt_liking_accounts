# Pro-Russian 'liking' accounts on Twitter

<img align="right" width="400" alt="image" src="https://user-images.githubusercontent.com/11286959/160737626-45c5c58c-88c2-4c3c-bfcc-7631307f89c0.png">

Account IDs and instructions for how to reproduce [my analysis of Twitter accounts](https://www.abc.net.au/news/science/2022-03-30/ukraine-war-twitter-bot-network-amplifies-russian-disinformation/100944970) that liked tweets from Russian government and embassy accounts.

## Step 1

The IDs of all accounts are provided in the repository as a text file: `liking_ALL_users_account_IDs.txt`.

There are 196689 unique accounts in total, which 'liked' at least one of the most recent 50 tweets from 75 Russian government and embassy accounts (details below). 

## Step 2

For the [bot analysis](https://twitter.com/timothyjgraham/status/1508029324334870528) I used the [Botometer model via the API](https://rapidapi.com/OSoMe/api/botometer-pro).

Specifically, I ran Botometer on 16513 accounts in the dataset that were created in 2022. The 'free' plan has a rate limit of checking 2000 accounts per day and there is a hard limit of 17,280 accounts per day which is due to the rate limits of the Twitter API itself. Therefore, I focussed attention on the most recently created accounts, many of which were created on the day Russia invaded Ukraine (24th February 2022).

You will need to run Botometer on the account IDs provided in Step 1, or a subset (e.g. accounts created in 2022). I did this in Python but it is possible to do it using other methods too, and [Botometer provides instructions](https://rapidapi.com/OSoMe/api/botometer-pro/details) for how to run the model.

## Step 3 (optional)

You can use the list of accounts IDs provided in Step 1 to collect all the account information via the Twitter API. Personally I use the [twarc2 software](https://twarc-project.readthedocs.io/en/latest/twarc2_en_us/) and the following command to collect user information for a set of IDs:

```
twarc2 users liking_ALL_users_account_IDs.txt liking_ALL_users_account_IDs.jsonl
```

## Notes

The accounts in this analysis 'liked' at least one of the most recent 50 tweets sent by 75 Russian government and embassy accounts detailed below. The most recent 50 tweets for each of the 75 accounts were collected on 19 March 2022. I used twarc2 to collect the timelines of these accounts (see Step 3 for more information about this data collection method).

1.	rusembusa
2.	rusembassyj
3.	rusembindia
4.	rusembjakarta
5.	rusembassyiraq
6.	rusemb_pl
7.	rusembest
8.	rusembethiopia
9.	rusembswiss
10.	rusembau
11.	rusembassynl
12.	rusembassykabul
13.	rusembsg
14.	rusembpakistan
15.	rusemb_iceland
16.	embrusbotswana
17.	rusembbangkok
18.	rusembbrunei
19.	rusembbul
20.	rusembbah
21.	rusembbih
22.	rusembcyprus
23.	rusembcro
24.	rusembcanada
25.	rusembchile
26.	rusembchina
27.	rusembdk
28.	rusembdprk
29.	rusembassy
30.	rusemberitrea
31.	rusembegypt
32.	rusembghanaeng
33.	rusembghana
34.	rusembhungary
35.	rusembitaly
36.	rusembindia_ru
37.	rusembjordan
38.	rusembkuw
39.	rusembkg
40.	rusembleb
41.	rusemblux
42.	rusembmalta
43.	rusembmanila
44.	rusembmauritius
45.	rusembmng
46.	rusembnigeria
47.	rusembnz
48.	rusembnam
49.	rusembperu
50.	rusembrso
51.	rusembsrilanka
52.	rusembsyria
53.	rusembswe
54.	rusembsey
55.	ambrusslo
56.	rusembsk
57.	rusembsrilankar
58.	rusembtz
59.	rusembturkey
60.	rusembuganda
61.	rusembusapress
62.	rusembukraine
63.	rusembvietnam
64.	emb_rus
65.	rusembz
66.	mission_russian
67.	sovfedinfo
68.	kremlinrussia
69.	embassyofrussia
70.	mid_rf
71.	natomission_ru
72.	mod_russia
73.	russia
74.	russiaun
75.	russianembassy

