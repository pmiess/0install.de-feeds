# 0install.de feeds

http://0install.de/feeds/ is a curated collection of [Zero Install](http://0install.net/) feeds for open-source and freeware applications. Most target Windows or are cross-platform.

This Git repository tracks changes to these feeds. We use a number of tools to help us manage the content:

[0template](https://github.com/0install/0template) is used to add new releases of applications. It takes a template (e.g., `VLC.xml.template`) and values for placeholders (e.g., a version number) as input and generates a new feed (e.g., `VLC-2.0.0.xml`) as output.

[0watch](https://github.com/0install/0watch) scrapes upstream websites to discover new versions of applications. It runs a watch file (e.g., `VLC.watch.py`) and then automatically calls 0template as needed.

[0repo](https://github.com/0install/0repo) manages the feeds themselves. It merges feeds generated by 0template (e.g., `VLC-2.0.0.xml`) into existing feeds (e.g., `VLC.xml`). It then generates GPG-signed versions of the feeds for hosting.