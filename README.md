# Dummy EPG xml Generator

### This bash Script Creates a dummy epg for use with channels that always have the same program

* You can add as many channels as you want, by adding more channel variables.
* The Dummy will, by default, generate programs for the next 2 days, with intervals of 6 hours between programs.


### How To Run:
* Fix the variables as you like
* go to the folder and execute the script ```./dummycreator.sh```
* You can automatically run int, using a cron job. The example bellow runs it every day at midnight:
```
0 0 * * * /bin/bash /file/location/dummycreator.sh
```
* After you are done, you can use a tool such as xmltv to merge it into your regular epg
```
tv_merge -i dummy.xml -m yourepg.xml -o merged.xml
```
