# Ubuntu Hangups Lib
[Ubuntu Hangups](https://github.com/tim-sueberkrueb/ubuntu-hangups) Dependencies 

## Update

* Run from the repository directory:
  ```
  python3 get_libs.py
  ```
* Download the sources of the following python packages and include them in `py/`:
  * [aiohttp] (https://github.com/KeepSafe/aiohttp)
  * [purplex] (https://github.com/mtomwing/purplex)
  * [requests] (https://github.com/kennethreitz/requests)
  * [pymmh3.py] (https://github.com/wc-duck/pymmh3)
  * [reparser] (https://github.com/xmikos/reparser)
  * [dateutil] (https://github.com/dateutil/dateutil)
  * [google.protobuf] (https://github.com/google/protobuf)
  * [appdirs] (https://github.com/ActiveState/appdirs)
  * [mechanicalsoup] (https://github.com/hickford/MechanicalSoup)
  * [beautifulsoup4] (https://pypi.python.org/pypi/beautifulsoup4)

* Remove line 1 in py/google/__init__.py. Otherwise the following permission error occurs:
```
  File "/opt/click.ubuntu.com/ubuntu-hangups.timsueberkrueb/0.3/lib/py/google/__init__.py", line 1, in <module>
    __import__('pkg_resources').declare_namespace(__name__)
    ...
  File "/usr/lib/python3/dist-packages/pkg_resources/__init__.py", line 2076, in find_on_path
    for entry in os.listdir(path_item):
  PermissionError: [Errno 13] Permission denied: '/usr/local/lib/python3.4/dist-packages'
```
