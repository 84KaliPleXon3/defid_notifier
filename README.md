# defid_notifier: Defacer.ID Mass Notifier
[![Python 2.6|2.7](https://img.shields.io/badge/python-2.6|2.7-yellow.svg)](https://www.python.org/) [![License](https://img.shields.io/badge/license-GPLv3-red.svg)](https://raw.githubusercontent.com/p4kl0nc4t/defid_notifier/master/LICENSE)

defid_notifier is a simple tool used to notify a lot of defacement at once. defid_notifier is running on Python 2.7.
## Installing.
You can install defid_notifier by cloning this repository or install it from PyPi by issuing `pip install defid_notfier`.
## Usage
```
usage: defid_notifier [-h] [--filter] [--verbose] [--timeout TIMEOUT]
                      [--start-at STARTAT] [--end-when ENDWHEN] [--turbo]
                      websites_list nick team

defid_notifier is a tool used to notify a lot of defacement at once (mass) to
Defacer.ID (https://defacer.id/).

positional arguments:
  websites_list       path to websites list
  nick                nick to be notified
  team                team to be notified

optional arguments:
  -h, --help          show this help message and exit
  --filter            show only successful notification
  --verbose           increase the verbosity (include response from server)
  --timeout TIMEOUT   set how long client waits for response (default: 60)
  --start-at STARTAT  set notifier's start point (line number)
  --end-when ENDWHEN  set maximum website to be notified from the start point
  --turbo             use TURBO mode, this mode uses same number of thread as
                      the number of website in websites list. Warning! TURBO
                      mode will consume a lot of memory depending on number of
                      threads. It is recommended to just set website limit.
```
## Turbo Mode
Turbo mode is using low level threading library "thread". Amount of thread depends on how much websites in your websites list. This mode is still buggy because of forever loop at the end. I will fix it as soon as possible.
## NodeJS Dependency
Hence defid_notifier is using cfscrape, NodeJS is required to run javascript code. On most debian system, you can install it by running ```apt-get install nodejs```.
