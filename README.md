# Backloggd.com csv Importer

Quick and dirty Python script for importing games from a csv file into [Backloggd.com](https://www.backloggd.com).
You will almost certainly need to adapt the code a little bit to make it work for your needs.

## backloggd.json
Next to the python script should be a configuration file, `backloggd.json`, set up as follows:
```
{
	id: [IGDB API ID],
	secret: [IGDB API Secret],
	backloggd_id: [Backloggd account ID],
	csrf: [Backloggd csrf token],
	cookie: [Backloggd cookie]
}
```
Your backloggd account ID can be found by inspecting most requests made on the site in a browser.
The csrf token can be found by inspecting the source on most site pages, or in most requests.
The cookie can be found in your browser's cookie settings. You are looking for the value to the key "_backloggd_session".
Note that the csrf and cookie tokens do expire, but not for a while. You should have no issue importing all your games at once before they need replacing.

## csv format
An example csv is provided. The default format is below, although it is very easy to adjust the code for your own needs.

Game Name | Platform | Played? | Playing? | Backlog? | Wishlist? | Status | Rating (out of 10)
----------|----------|---------|----------|----------|-----------|--------|-------------------
Ikaruga | Dreamcast | false | false | true | false | completed | 
Pokemon Yellow | Game Boy | true | false | false | false | completed | 9
Metroid Zero Mission | Game Boy Advance | true | false | false | false | retired | 9
Pokemon Crystal | Game Boy Color | true | false | false | false | shelved | 9
Another Code | Nintendo DS | true | false | false | false | abandoned | 7
Ace Attorney Trials and Tribulations | Nintendo DS | true | false | false | false | played | 8
Mother | Nintendo Entertainment System | false | false | true | false | completed | 
