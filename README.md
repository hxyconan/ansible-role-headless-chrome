# ansible-role-headless-chrome

An ansible role to install latest headless google-chrome and chromedriver on Ubuntu server. 

## Intro
- New Chrome (versions greater than or equal to 59) supports headless automation tests, which usually done via PhantomJS headless browser.
- PhantomJS, as traditionally headless browser will not be maintained anymore. [Chrome is faster and more stable than PhantomJS. And it doesn't eat memory like crazy](https://groups.google.com/forum/#!topic/phantomjs/9aI5d-LDuNE).
- You can have your Selenium WebDriver setup (which has not been coverred in this anisble role) and running with Chrome in its headless mode.


## Features
- A [chromedriver](https://sites.google.com/a/chromium.org/chromedriver/) bin installed to drive google-chrome, it is required by automation testing script which will check the driver at http://localhost:9515/
- Upstart service "chromedriver" installed and will start automatically after reboot


## How to use
- start\stop\restart the application as:

```
sudo service chromedriver start|stop|restart
```

- Check status via 

```
sudo service chromedriver status
```


## Testing Environment
- Ubuntu 14.04.5 LTS (GNU/Linux 3.13.0-110-generic x86_64)


## Reference:
- [https://developers.google.com/web/updates/2017/04/headless-chrome](https://developers.google.com/web/updates/2017/04/headless-chrome)
- [https://tecadmin.net/install-google-chrome-in-ubuntu/](https://tecadmin.net/install-google-chrome-in-ubuntu/)
- [https://intoli.com/blog/running-selenium-with-headless-chrome/](https://intoli.com/blog/running-selenium-with-headless-chrome/)

