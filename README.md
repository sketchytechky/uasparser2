Fast and reliable User Agent parser for python
==============================================
Author: Jure Ham (jure.ham@zemanta.com)

- Tested with more the 50.000 unique user agents.
- Up to date data provided by http://user-agent-string.info/
- Built-in simple cache.


Forked from:
---------
A python version of http://user-agent-string.info/download/UASparser

By Hicro Kee (http://hicrokee.com) email: hicrokee AT gmail DOT com

Modified by Michal Molhanec http://molhanec.net


Usage:
------
	from uasparser2 import UASparser

	uas_parser = UASparser('/path/to/your/cache/folder', mem_cache_size=1000)

	result = uas_parser.parse('YOUR_USERAGENT_STRING')

	# If input data is not avaible in cache folde, UASparser will download and prepare it on init.
	# Force data update by calling:

	uas_parser.updateData()


Speed comparison:
-----------------
Parsing 100,000 user agents (10,000 uniqe) from our server logs:

original uasparser: 7264.2 sec

uasparser2 without cache: 184.5 sec

uasparser2 with cache(size 1000): 35.9 sec
