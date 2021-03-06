###Status
[![Build Status](https://travis-ci.org/szabgab/codeandtalk.com.png)](https://travis-ci.org/szabgab/codeandtalk.com)

List of tech conferences, podcasts, videos, people
==================================================

For more details visit:

[Events](docs/CONFERENCES.md)

[Videos](docs/VIDEOS.md)

[Podcasts](docs/PODCASTS.md)

[People](docs/PEOPLE.md)

SETUP
------
```
virtualenv venv -p python3
source venv/bin/activate
pip install --editable .
```

Generate web site (and check format)
-----------------------------------
```
$ python3 bin/generate.py
```

Development server
-------------------
```
export FLASK_APP=cat.app
export FLASK_DEBUG=1
flask run --host 0.0.0.0 --port 5000

FLASK_APP=cat.app FLASK_DEBUG=1 flask run --host 0.0.0.0 --port 5000
```

```

http://localhost:5000/

TODO
-----

These are just ideas, not necessary something I really want to do :-)

* check if there is 'view' and 'like' in the video files, not just 'length'.

* Generate Calendar of events
  - for each geographic area (e.g. Europe)
  - Shall we include the cfp deadlines or not?

* improve the search for people
* improve the search for videos
* show number of videos in the list of people
* tags should be all lower case in the files and we should have the real case in the tags file. That will make the code simpler


* For each event series find out if they have an annuncement mailing list to get notified for the new event, cfp,  videos available.
Add this information to the data/series.json file Talk to the organizers and tell them why we would like to get such notifications.

* Describe the use of the site.
* Convert all the data files to JSON, beautify them?
* Create skeleton for each file-type?

* Include picture of each speaker?
* Include logo of each event?

* Change the sitemap.xml creating code to use the date of the files for real date.
* For sitemap of the collection pages, use the timestamp of the most recent event in that list.
* For sitemap of videos, use the date of the file.

* Update the description of the data and the collection process.

* Search:
  limit the search to people/videos/events/podcasts

* Search for videos
  limit the search by date
  limit the search by language (for videos)


* Weekly Newsletter with information about events.
  The subscriber should be able to select filter by countries and/or by topics.
  The e-mail itself is an HTML message that we can also build on the website.

* Add Facebook image code to video pages
* Improve the UI of the web site, look at what pyvideo has nice.
* Link from event to other events in the series.

* Another potential use of the data: Help conference and meetup organizers find potential speakers.
* List people by location (city, state, country)
* List people by subjects (tags for which they spoke)

* Add "language" field to the videos and allow the user to filter the results to selected language(s). (There are talk in French, German, Spanish, etc.)

* Include the number of videos in the https://codeandtalk.com/people list
* Create list of people with 0 in everything bin/people.py
* List of people who only have their name in the file
* List of people missing twitter/github

 
* Include screencasts and other non-conference videos.
* Include a picture of each person?


TODO Check for events:
-------------
* http://2016.geecon.cz/
* http://www.qualitysoftware.com.au/ http://www.qualitysoftware.com.au/atd2k16/
* http://europeantestingconference.eu/2017/ https://twitter.com/EuroTestingConf
* http://codecooperative.org/
* https://central.wordcamp.org/
* https://wpcampus.org/
* https://therichwebexperience.com/conference/clearwater/2016/12/home
* http://www.cue.org/conference
* http://www.nodetogether.org/
* https://atscaleconference.com/
* https://jsconf.co/2015-Videos/
* http://rubycentral.org/railsconf

* https://www.youtube.com/channel/UCp2Tsbjd3P8itnBHUNHi82A/playlists
* https://github.com/nodeconf

http://visualized.com/2014/conference/
http://visualized.com/2015
http://visualized.com/2016

[ReactJS-IL] YouTube Channel for Recorded Talks : https://www.youtube.com/channel/UC7AkWgJFP_hBoU0M7_n0prQ



Other sources
------
https://techpoint.ng/2016/09/14/hackjos-2016-2/


Promotion
------------
After watching videos, they might be promoted via various channels.

* Posted to the appropriate subredit at https://www.reddit.com/
* Posted at HackerNews: https://news.ycombinator.com/
* Marked as "featured" and included in one of the blasters: https://codeandtalk.com/blasters
* Tweeted via https://twitter.com/codeandtalk
* Posted on the Facebook page: https://facebook.com/CodeAndTalk


Some Advice to Conference organizers
--------------------------------------
Just a few random thoughts as I index the videos and the conferences.

* If you record lightning talks, split them up to individual videos. That allows people to watch one short video while at work.
* Include the names of the speakers in the filenames.

* Keep the web site of the previous editions of your event, or at least keep the list of talks and list of people.
* The best would be to have well defined URLs. Some conferences have subdomains per year: http://2017.someevent.com/
Other have them in subdirectory: http://someevent.com/2017/  Both are good.
The best if the main page only redirects to the current event or holds some content, but each event has its own subsite.
Make sure every page of the earlier events have a prominent link at the top linking to the home page of the conference (which can then
redirect to the current or upcoming event).

* On the speaker page include the Twitter and GitHub IDs of each speaker.


Ideas for Conferences and other events
---------------------------------------
* Givng a talk (ok, this is the obvious)
* Improv sessions https://codeandtalk.com/v/agile-india-2016/3-minute-improv-games-to-improve-your-teams-by-wayde-stallmann
* Matching up mentors and mentees https://codeandtalk.com/v/clojure-conj-2016/overcoming-the-challenges-of-mentoring-kim-crayton
  The idea would be to do a much shorter talk and spend a lot more time on matching mentors and mentees.
* Building a startup around conversations and communities
  https://codeandtalk.com/v/agile-india-2016/building-a-startup-around-conversations-and-communities-by-zainab-bawa
* Personal vision exercise: https://codeandtalk.com/v/agile-india-2016/giving-the-enterprise-focus-through-a-compelling-shared-vision-by-susan-gibson

* Mostly after hours:
  * BOF (Birds of Feather) sessions - people can organize meetings based on a specific subject.
  * Dinner with all the attendees
  * Speaker's dinner (can provide a place to socialize)
  * Hackathons - these usually happen on the day(s) before or after the conference, but not during the conference.
      They also seem to be a bit solitary programming.
  * Game night (playing board games, cards) just socializing
* Scavenger hunt (described in AB Testing podcast episode 48-49 https://github.com/szabgab/ab-testing


Process with command line Git client
----------------------------
* In the GitHub interface visit the project https://github.com/szabgab/codeandtalk.com and click on the "Fork" button (top righ).
It will create a copy in your own user. IF you are called ```foobar``` it will be called https://github.com/foobar/xcast

* On your command line (Linux terminal or Windows Cmd) type in

```git clone git@github.com:foobar/xcast.git```

It will clone (copy) the whole repository from your GitHub homedirectory.

```cd xcast```

```git remote add upstream https://github.com/szabgab/xcast.git```

Now you can edit the files in the ```xcast/data``` directory and add more files you need.

If you'd like to check if the files work well together type in

```python xcast.py --html``` on windows or ```python3 xcast.py --html``` on Linux.



Instruction on Windows
----------------------
* Install Python 3.x.x from https://www.python.org/downloads/windows/
* Open the command window (Start/Run 'cmd')
* Type in ```python --version``` to check if the installation worked as expected. It should say something like "Python 3.5.2"
  If it says "`Python` is not recognized as an internal or external command, operable program or batch file"
  then you need to configure the PATH environment variable to include the directory of python.exe
  One way is to enter the following in the command prompt: just replace 'gabor' with your username:
  ```set PATH=C:\Users\gabor\AppData\Local\Programs\Python\Python35-32\;%PATH%```
  Then try ```python --version``` again.

* Type in ```pip install jinja2```
* cd to the xcast/ directory 
* Type ```python xcast.py --html```   If there is an error in the files, it will complain.
* If everything works fine the web site is generated in the html/ directory.
* Run ```python server.py``` then go to your broser and visit http://127.0.0.1:8000/  The updated site should be there.
