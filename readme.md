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
