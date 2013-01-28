Deildu.net Search Provider Add-on for Sick Beard
=====

This is a fork of the PirateBay branch from the Sick Beard repo, a Deildu.net Search Provider add-on for Sick Beard, based on 
ThePirateBay add-on.

## Installation

*These instructions assume you already have SickBeard setup, so we also take in to consideration copying the SickBeard database and config. If you're setting SickBeard up for the first time, simply ignore those steps.*

```
# Back up existing SickBeard folder
mv sickbeard sickbeard_old
# Kill SickBeard
cd /tmp
wget -q "http://127.0.0.1:8081/home/shutdown/"
# Download trymbill's Deildu branch
cd ~
git clone https://github.com/trymbill/Sick-Beard.git sickbeard-deildu
# Copy old settings over to new installation
cp sickbeard_old/sickbeard.db sickbeard-deildu
cp sickbeard_old/config.ini sickbeard-deildu
cp sickbeard_old/autoProcessTV/autoProcessTV.cfg  sickbeard-deildu/autoProcessTV
# Start new Deildu.net SickBeard
python sickbeard-deildu/SickBeard.py -q > /dev/null 2>&1 &
# All done
```

*Note that these instructions are based on locations you might not want to use, like storing sickbeard in your home directory, calling it sickbeard-deildu, etc. Instructions are only for reference, use at your own risk.*



Original Sick Beard Readme
=====

*Sick Beard is currently an alpha release. There may be severe bugs in it and at any given time it may not work at all.*

Sick Beard is a PVR for newsgroup users (with limited torrent support). It watches for new episodes of your favorite shows and when they are posted it downloads them, sorts and renames them, and optionally generates metadata for them. It currently supports NZBs.org, NZBMatrix, Bin-Req, NZBs'R'Us, EZTV.it, and any Newznab installation and retrieves show information from theTVDB.com and TVRage.com.

Features include:

* automatically retrieves new episode torrent or nzb files
* can scan your existing library and then download any old seasons or episodes you're missing
* can watch for better versions and upgrade your existing episodes (to from TV DVD/BluRay for example)
* XBMC library updates, poster/fanart downloads, and NFO/TBN generation
* configurable episode renaming
* sends NZBs directly to SABnzbd, prioritizes and categorizes them properly
* available for any platform, uses simple HTTP interface
* can notify XBMC, Growl, or Twitter when new episodes are downloaded
* specials and double episode support


Sick Beard makes use of the following projects:

* [cherrypy][cherrypy]
* [Cheetah][cheetah]
* [simplejson][simplejson]
* [tvdb_api][tvdb_api]
* [ConfigObj][configobj]
* [SABnzbd+][sabnzbd]
* [jQuery][jquery]
* [Python GNTP][pythongntp]
* [SocksiPy][socks]
* [python-dateutil][dateutil]
* [jsonrpclib][jsonrpclib]
* [Subliminal][subliminal]
* [IMDbpy][imdbpy]

## Dependencies

To run Sick Beard from source you will need Python 2.6+ and Cheetah 2.1.0+. The [binary releases][googledownloads] are standalone.

## Bugs

If you find a bug please report it or it'll never get fixed. Verify that it hasn't [already been submitted][googleissues] and then [log a new bug][googlenewissue]. Be sure to provide as much information as possible.

[cherrypy]: http://www.cherrypy.org
[cheetah]: http://www.cheetahtemplate.org/
[simplejson]: http://code.google.com/p/simplejson/ 
[tvdb_api]: http://github.com/dbr/tvdb_api
[configobj]: http://www.voidspace.org.uk/python/configobj.html
[sabnzbd]: http://www.sabnzbd.org/
[jquery]: http://jquery.com
[pythongntp]: http://github.com/kfdm/gntp
[socks]: http://code.google.com/p/socksipy-branch/
[dateutil]: http://labix.org/python-dateutil
[googledownloads]: http://code.google.com/p/sickbeard/downloads/list
[googleissues]: http://code.google.com/p/sickbeard/issues/list
[googlenewissue]: http://code.google.com/p/sickbeard/issues/entry
[jsonrpclib]: https://github.com/joshmarshall/jsonrpclib
[subliminal]: https://github.com/Diaoul/subliminal
[imdbpy]: https://github.com/alberanid/imdbpy
