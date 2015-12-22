# HaleTracks
#####V1.1

Simple and dynamic boss statistics tracker for Freak Fortress 2 based servers.

Supports HTTP upload with JSON and local stat storage with the VDF KeyValues file format.

| Supported Stats  |
| ------------- |
| Hale Name      |
| Win or Loss     |
| Average Boss Ping |
| Mercenary Count |
| Map |
| Server Hostname |
| Server Public IP |
| Full Health |
| Health on round end |


HaleTracks can detect all forms of triggered suicide, such as the 'kill' command.
By default, triggered suicide will throw out the the round data to preserve overall data accuracy.

Installation:


  Download .smx plugin, then drag-n-drop to your tf/addons/sourcemods/plugins directory.
  Download haletracks_config.txt, place it in tf/addons/sourcemod/config directory.
      -HaleTracks will create a default config file on first run, if this step is skipped.
  
  Open haletracks_config.txt, consult the convars list below.


  If you're using a custom version of FF2, you may have to compile the .sp file, replacing
  the freak_fortress_2 includes to your version.

Example JSON uploaded:
```json
{ 
	"haletracks": {
		"version": "1.1",
		"hostname": "Test Futon",
		"address": "74.127.175",
		"map": "arena_badlands",
		"starttime": "12-21-15 23:28:00", 
		"endtime": "12-21-15 23:31:24", 
		"winteam": 2,
		"winreason": 2,
		"bluescore": 0,
		"redscore": 7, 
		"mercs": { 
			"team": "2", 
			"startcount": "5", 
			"endcount": "5", 
			"inroundspawns": "1", 
			"deaths": "0", 
			"disconnects": "0", 
			"classdamage": { 
				"scout": { 
					"damage": 0,
					"ffdamage": 0
				}, 
				"soldier": { 
					"damage": 6292,
					"ffdamage": "0"
				},
				"pyro": { 
					"damage": 0,
					"ffdamage": 0
				},   
				"demoman": { 
					"damage": 0,
					"ffdamage": 0
				}, 
				"heavy": { 
					"damage": 0,
					"ffdamage": 0
				},
				"engineer": { 
					"damage": 0,
					"ffdamage": 0
				},   
				"medic": { 
					"damage": 0,
					"ffdamage": 0
				}, 
				"sniper": { 
					"damage": 0,
					"ffdamage": 0
				},
				"spy": { 
					"damage": 0,
					"ffdamage": 0
				 } 
			} 
		}, 
		"hales": {
			"team": 3, 
			"haletitle": "Vagineer",
			"afkcount": 1, 
			"suicidecount": 0, 
			"disconnectcount": 0, 
			"botcount": 1,  
			"haledropped": false, 
			"nohale": false, 
			"halelist": {
				"0": {
					"title": "Vagineer",
					"health": 0,
					"maxhealth": 6074,
					"lives": 1,
					"maxlives": 1,
					"isafk": true,
					"isbot": true,
					"issuicide": false,
					"isdisconnect": false
				}
			}
		},   
		"minions": {
			"startcount": 0,
			"endcount": 0,
			"inroundspawns": 0,
			"deaths": 0,
			"disconnects": 0,
			"damagecount": 0,
			"ffdamagecount": 0 
		}       
	} 
}
```


