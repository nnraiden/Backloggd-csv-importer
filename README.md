# Backloggd.com csv Importer

It works for me. Requires the addition of new columns after gameID match.

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
Backloggd ID can be found by inspecting network requests. Look into any html, should be defined under cdn-uid. You can find your cookie in the same html, under cookies. Find your csrf by vieweing page source, search for csrf.

## csv format
Look at the provided file.

## limitation
adds games as played.
