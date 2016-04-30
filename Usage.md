Below are some examples of usage. You can download the latest API docs  [here](http://code.google.com/p/pygeoip/downloads/list).

## Country Database (`GeoIP.dat`) ##

```
>>> import pygeoip
>>> gi = pygeoip.GeoIP('/path/to/GeoIP.dat')
>>> gi.country_code_by_name('google.com')
'US'
>>> gi.country_code_by_addr('64.233.161.99')
'US'
>>> gi.country_name_by_name('google.com')
'United States'
>>> gi.country_name_by_addr('64.233.161.99')
'United States' 
```


## City Database (`GeoIPCity.dat`) ##

```
>>> import pygeoip
>>> gic = pygeoip.GeoIP('/path/to/GeoIPCity.dat')
>>> gic.record_by_addr('64.233.161.99')
{'city': 'Mountain View', 'region_name': 'CA', 'area_code': 650, 'longitude': -122.0574, 'country_code3': 'USA', 'latitude': 37.419199999999989, 'postal_code': '94043', 'dma_code': 807, 'country_code': 'US', 'country_name': 'United States'}
>>> gic.record_by_name('google.com')
{'city': 'Mountain View', 'region_name': 'CA', 'area_code': 650, 'longitude': -122.0574, 'country_code3': 'USA', 'latitude': 37.419199999999989, 'postal_code': '94043', 'dma_code': 807, 'country_code': 'US', 'country_name': 'United States'}
>>> gic.region_by_name('google.com')
{'region_name': 'CA', 'country_code': 'US'}
>>> gic.region_by_addr('64.233.161.99')
{'region_name': 'CA', 'country_code': 'US'}
>>> gic.time_zone_by_name('google.com')
'America/Los_Angeles'
>>> gic.time_zone_by_addr('64.233.161.99')
'America/Los_Angeles'
```

## Org/ISP Database (`GeoIPOrg.dat` or `GeoIPISP.dat`) ##

```
>>> import pygeoip
>>> gio = pygeoip.GeoIP('/path/to/GeoIPOrg.dat')
>>> gio.org_by_addr('64.233.161.99')
'Google'
>>> gio.org_by_name('google.com')
'Google'
```

## Region Database (`GeoIPRegion.dat`) ##

```
>>> import pygeoip
>>> gir = pygeoip.GeoIP('/path/to/GeoIPRegion.dat')
>>> gir.region_by_name('yahoo.com')
{'region_name': 'CA', 'country_code': 'US'}
>>> gir.region_by_addr('209.131.36.159')
{'region_name': 'CA', 'country_code': 'US'}
```