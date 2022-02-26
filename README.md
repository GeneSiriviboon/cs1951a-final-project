# cs1951a-final-project
Group: Michelle-and-the-weebs

## Data Spec

First, the popular animes are extracted by ranking using MAL API [https://api.myanimelist.net/v2/anime/ranking] which give us the following

- 'node': json of 
    - 'id': integer of anime's primary key 
    - 'title': string of anime name
    - 'main_picture': json containing the medium and large icon of the anime poster (not used)
- 'ranking': json of
    - 'rank' : integer

From the dataset, we create a pandas table containing XXX rows of id, rank, and title

The details of the animes are then extracted from another MAL API [https://api.myanimelist.net/v2/anime/{anime_id}] with the following columns

- 'id': integer of anime's primary key  (match from ranking data)
- 'title': string of anime name
- 'genres': list of genre of the anime including 
    - XXX
- 'mean': number or null of mean rating (null if too small sample size)
- 'nsfw': 'white' | 'grey' | 'black' describing whether the anime is safe for work.
- 'popularity': integer 
- 'status'
- 'num_list_users': Number of users who have this work in their list.
- 'related_anime': list of ids of the related anime
- 'rating': age rating of the anime (string)
    - g 	G - All Ages
    - pg 	PG - Children
    - pg_13 pg_13 - Teens 13 and Older
    - r 	R - 17+ (violence & profanity)
    - r+ 	R+ - Profanity & Mild Nudity
    - rx 	Rx - Hentai
- 'media_type' 
    - unknown
    - tv
    - ova
    - movie
    - special
    - ona
    - music
- 'synopsis': string summarizing the plot and premises of the anime


## Potential Area of Exploration
- create a network of related anime from the first XXX most popular anime and study its topology
- rating vs. mean vs. statistics

## Roadblocks
- can only extracted up to 100 most popular animes.

