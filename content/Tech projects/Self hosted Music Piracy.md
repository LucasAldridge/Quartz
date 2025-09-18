I want a way to pirate my music and play it locally. Woke mfs are moving away from Spotify because of the CEO's AI war drone investment, so what's a better time to make an army of scrapers to create a user-friendly solution to music streaming. 
# Goals
- Make the switch from Spotify to my network EASY
- Search function for music
- Something that ensures you get the BEST quality possible. 

### What I'm NOT doing
- Creating a physical device to play music
- Writing something that will run on an iphone, ipod, or really any handheld device 

# Steps
- [ ] Get a list of every music pirating website i possibly can 
- [ ] Become better versed in webscraping (Learn limits)
- [ ] Determine which I can write scrapers for (This part makes or breaks the project)
- [ ] Write scrapers
- [ ] Research how to ensure the file is actually the right music and is of good quality
- [ ] Write a tool to do the above
- [ ] Understand how playlists work on most platforms from a back-end perspective
- [ ] Find a way to let user input playlist (non-manually) and scrape for each song. Format appropriately. 
- [ ] Research how to make a good search tool that doesn't just take search term at face value but returns options that are close to user's input (EX: input "I LAY DOWN MY LIFE FOR YOU" returns not only the original version of the album, but the director's cut as well)
- [ ] Create search tool that calls scrapers and calls quality check
- [ ] Ensure there is an easy way to manage downloaded music. 
- [ ] Front-end?
- [ ] Research Torrenting shit
- [ ] Write Torrenting shit

# What the end product should look
This is for CLI specifically
- Program starts
- Instructions are presented, explains the commands 
	- Search - runs the search tool
	- Playlist - runs playlist conversion tool
	- Files - Opens file location where downloaded music has been stored
	- Wipe - Prompts confirming that the path to the music downloads folder is correct and that you ACTUALLY wanna delete it
	- Torrent - Explains what torrenting is, how it works, safe torrenting, and then confirms you want to turn it on

# What Next?
At the time of writing this, I intend for it to be open source. That means I cant do anything like charge for it or anything like that. Obviously it would be really nice to make money, but people pirating music aren't really in the business of giving it out. So since I'm not gonna do everything I can to make a ton of money... how can I take this project a step further in making music more and more accessible? Torrenting. Tommy planned to do this for his movie/TV scraper and I think I'll do something similar. I want to give myself and everyone else who uses the tool to seed the music files they download IF THEY WANT. This will not be mandatory, nor will it be something you just type a command and start doing. There are inherent dangers to torrenting when not done properly, and I don't want those to befall people who don't know what they're doing. More than likely I will write or locate a safe torrenting guide and force it to display before they can turn on the setting. 

## Architecture
The flow may work like this...
- search prompt
- search prompt goes to all scrapers
- scrapers convene at ranker, show all their results and the ranker ranks all of it based off their source scores and quality of their results
- highest ranked is served 
- user can change if they want but that hurts that source's score

Choose source
top... 10 results from there are chosen. first source given is chosen by ranking system. thats where switch occurs. playback is handled in bg. 


SO
- search prompt
- if prompt hella similar to some shi in cache we show them the cached song first
- search prompt goes to all scrapers
- top ranked source has its results shown first. 
- full play event gives points, the earlier the result is in the list the greater the points
- non-full play takes off js a few points
- changing source is BAD for points

SO FOR EACH SCRAPER
it needs to get name, artist name, duration, and a means to download the selected song
