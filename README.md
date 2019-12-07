Retweet Bot
==================

![alt text](https://img.shields.io/badge/python-3.7-green.svg "Python3.7") ![alt text](https://img.shields.io/badge/tweepy-3.7-green.svg "tweepy3.7")

This script retweets certain tweets with a specific search query and can use parameters defined in the config file to perform additional actions. To limit Twitter requests it uses a savepoint for each configured query objects, search query id and marks the last tweet it retweeted. 

It's Twitter API v1.1 ready.

Requirements:
-------------
You need Python 3.4 or later to run mypy. You can have multiple Python versions (2.x and 3.x) installed on the same system without problems.

To download Python 3.4 on Linux, OS X and Windows, packages are available at

  http://www.python.org/getit/

Dependencies:
-------------
Install the dependencies like this:

   ```pip install -r requirements.txt```

Quick start:
-------------

To start create a copy of ```config.SAMPLE.json``` and rename to ```config.json```, then follow the steps below.
* In ```config.json``` define your ```query_objects``` in the config file. See https://git.io/vNqUv for an example
* In ```config.json``` define your ```twitter_keys``` to the config file. Find these at https://apps.twitter.com/

If Python is installed correctly and your ```config.json``` file is setup, you can run the bot by using: 
* $ python retweet.py


Use as cron job
---------------

create file at 

```/etc/cron.d/retweetBot```

with the contents

```
30 * * * * [your-user-here] cd ~/retweet-bot/src/ && python3 main.py >> ~/retweet-bot/twitter_bot.txt
```

please use https://crontab.guru for more info on how to set time for cron jobs.

Working Example
---------------

‪https://twitter.com/AlderaanTechNet‬

Compatibility
-------------

Compatible with Python 3.7 && tweepy 3.7
