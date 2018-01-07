PyGRT v1.0.0
===============
|pypi| |build|

PyGRT is a thin API wrapper for the Grand River Transit Realtime API that isn't currently publicly documented. This is as much of the API as I could reverse-engineer/find in their public app.

Install
==============
To install PyGRT:
      
      pip install pygrt
      
Or:

      python setup.py install
      
Usage
==============
Currently there is no rate-limiting but the GPS data is updated every 30 seconds so retrieving data any faster than that is unecessary.

```python
  from pygrt import GRT

  grt = GRT()

  # Get all current bus information
  print(grt.bus.all())
  
  # Get bus info
  print(grt.bus.info('bus_id', 'trip_id')
```
