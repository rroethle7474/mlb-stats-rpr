## Installation

Install from PyPI using pip:

`pip install MLB-StatsAPI` or `python -m pip install MLB-StatsAPI`

Upgrade using pip:

`pip install --upgrade MLB-StatsAPI` or `python -m pip install --upgrade MLB-StatsAPI`

## Use 

First, import the package:

`import statsapi`

Then call the applicable [function](https://github.com/toddrob99/MLB-StatsAPI/wiki/All-Functions), such as `schedule`:

`sched = statsapi.schedule(start_date='07/01/2018',end_date='07/31/2018',team=143,opponent=121)`

## Logging

The MLB-StatsAPI module utilizes Python's standard Logging module, with the logger name `statsapi`. Set the appropriate log level and attach a log handler to the `statsapi` logger in order to see the logs. For example:

    import logging
    logger = logging.getLogger('statsapi')
    logger.setLevel(logging.DEBUG)
    rootLogger = logging.getLogger()
    rootLogger.setLevel(logging.DEBUG)
    ch = logging.StreamHandler()
    formatter = logging.Formatter("%(asctime)s - %(levelname)8s - %(name)s(%(thread)s) - %(message)s")
    ch.setFormatter(formatter)
    rootLogger.addHandler(ch)
