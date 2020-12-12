# heroku-integrated-firefox-geckodriver

Installation:
-----

To install and integrate the buildpack with your application running on Heroku's dyno:

```shell
$ heroku create --buildpack https://github.com/pierredemilly/heroku-integrated-firefox-geckodriver

# or if your app is already created:
$ heroku buildpacks:add https://github.com/pierredemilly/heroku-integrated-firefox-geckodriver

$ git push heroku master
```

Configurations:
-----

Update Heroku's environment variables to store the following path strings. 
                                
  
**FIREFOX_BIN**: */app/vendor/firefox/firefox*

**GECKODRIVER_PATH**: */app/vendor/geckodriver/geckodriver*

**LD_LIBRARY_PATH**: */usr/local/lib:/usr/lib:/lib:/app/vendor*

**PATH**: */usr/local/bin:/usr/bin:/bin:/app/vendor/*

                

These configuration vars can be updated via Heroku CLI as follows:

Executable command: `heroku config:set <ENV_VARIABLE>=<ABSOLUTE_PATH>`

```shell

$ heroku config:set FIREFOX_BIN=/app/vendor/firefox/firefox

Setting FIREFOX_BIN and restarting python-app... done, v6
FIREFOX_BIN: '/app/vendor/firefox/firefox'

```


Go ahead and scrape the universe. Drop a star if you like this small project!

<a href="https://ko-fi.com/F1F1VEXA" target="_blank"><img src="ko-fi.png" alt="Buy me a Ko-fi, will ya?!" width="200"/></a>
