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
        "data": {
            "server": {
                "hostname": "VS FutonVille V1",
                "ipv4": "192.938.384.83"
            },
            "hales": {
                "Rainbow Crash": {
                    "1": {
                        "map": "arena_badlands",
                        "wintype": 1,
                        "merccount": 30
                    },
                    "2": {
                        "map": "mc_village_beta",
                        "wintype": 3,
                        "merccount": 28
                    },
                    "3": {
                        "map": "2fort_desk",
                        "wintype": 0,
                        "merccount": 10
                    }
                },
                "Thi Barret": {
                    "1": {
                        "map": "crevice",
                        "wintype": 1,
                        "merccount": 30
                    },
                    "2": {
                        "map": "mc_village_beta",
                        "wintype": 1,
                        "merccount": 15
                    },
                    "3": {
                        "map": "2fort_desk",
                        "wintype": 2,
                        "merccount": 30
                    }
                }
            }
        }
    }
}
```

Example VDF local file storage
```
"haletracks"
{
  "version" "1.1",
  "data"
  {
    "server"
    {
      "hostname" "VS FutonVille V1"
      "ipv4" "192.938.384.83"
    }
    "hales"
    {
    "Rainbow Crash"
    {
        "1"
        {
          "map": "arena_badlands"
          "wintype": "1"
          "merccount": "30"
        }
        "2"
        {
          "map": "mc_village_beta"
          "wintype": "3"
          "merccount": "28"
        }
        "3"
        {
          "map": "2fort_desk"
          "wintype": "0"
          "merccount": "10"
        }
    }
    "Thi Barret": {
        "1"
        {
          "map": "crevice"
          "wintype": "1"
          "merccount": "30"
        }
        "2"
        {
          "map": "mc_village_beta"
          "wintype": "1"
          "merccount": "15"
        }
        "3"
        {
          "map": "2fort_desk"
          "wintype": "2"
          "merccount": "30"
        }
      }
    }
  }
}

```


