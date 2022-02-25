# siege-engine
A tactical piece of software that allows the magnificient company SMOK sp. z o. o. strike it's enemies from afar


Installation and operation
==========================

Just type:

```bash
pip install siege-engine
python -m siege_engine 300 tass.com
```

Note that a helpful error message will be displayed if you just type:

```bash
python -m siege_engine
```

Please set the 300 value regarding your network conditions. This is the amount of threads
that will be spawned. Obviously, more is better (I bet your network could hold about 2000
of them).

Note that increasing thread count about 100% CPU usage is pointless, because of the GIL.
You can, altogether, fire up multiple instances :D

Note that if zero connections were made, that means the target server is no longer responding,
which is a good thing.

# Change log

* v1.3: significantly refactored the code
* v1.2: since v1.1 we're been hosted on PyPI, removed these nasty entry points
* v1.1: added graceful support for time-out sessions