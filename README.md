#### Based on [Mp3tag-Sources](https://github.com/Onurtag/Mp3tag-Sources) by [Onurtag](https://github.com/Onurtag) that is based on [original script](https://community.mp3tag.de/t/ws-vocadb-net/17192) by PBX_g33k! Check [ORIGINAL_README.md](ORIGINAL_README.md) for more information

## Installation  
Requires Mp3tag v2.64 or above.  
.src files should be directly in your tag sources directory: **%APPDATA%\Mp3tag\data\sources**  
(like C:\Users\You\Appdata\Roaming\Mp3tag\data\sources)  

You can download all .src files using the **Code -> Download ZIP** button.  

## VocaDB Sources  


- #### VocaDB English Album.src:    
  - All names, titles and lyrics will be in English if they exist.   
  - JAPANESETITLE and JAPANESEALBUM tags will be added to each song.  
  - Appends "(Instrumental)" to instrumental track names
  - Inserts both ALBUMARTIST and ARTIST in a format that is compatible with id3v2's multiple artists using "\\\\" separator (You can change this to your liking)
  - Fixes date insertion from original repo
  - Fixes tracks counting
  - Inserts release event into VOCADB_RELEASE_EVENT tag, has support for multiple release events and separates them with "\\\\" separator. (You can change this to your liking)


- #### VocaDB English Song.src:  
  Should work similar to Album search, but also:
  - Allows to search for songs using both name **and** VocaDB Artist **Tag** (eg. [36280](https://vocadb.net/Ar/36280)) simultaneously to make up for listing maximum 100 search results
  - Shows info about found songs, including albums containing the song
  - Inserts thumbnail from VocaDB as cover image
  - Code should theoretically be ready to also show thumbnails in search results (primary screen if more than one song is found) when mp3tag will also allow this feature on Windows builds as mentioned [here](https://community.mp3tag.de/t/web-sources-search-thumbnails/59491).
&nbsp;
## UtaiteDB and TouhouDB Sources  
They should be the same as VocaDB sources and use UtaiteDB/TouhouDB links and tags instead.
TouhouDB also doesn't use "&preferAccurateMatches=true" when doing album api call, since its api seems to be a bit slower and using this in api calls often prolonged response time, which caused request timeouts
