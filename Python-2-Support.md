Support for Python 2 will be removed from the MLB-StatsAPI on or after January 1, 2021. The module may continue to function in Python 2, but any issues not impacting Python 3 will be closed. This change is likely to have an impact on string encoding, which may result in player names with non-ascii characters not being returned as expected. Specifically, I will be removing the following lines which apply only to Python 2:

```python
# Trying to support Python 2.7:
if sys.version_info.major < 3:
    reload(sys)
    sys.setdefaultencoding("utf8")
```

Python 2 has been officially unsupported since January 1, 2020. The MLB-StasAPI module will follow suit one year later.