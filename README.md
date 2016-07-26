# sabnzbd-influxdb-export

This script will query SABnzbd to pull basic stats and store them in influxdb. Stay tuned for further additions!

I suggest you intall the script as a service to boot with your OS.

## Dependencies
  * SABnzbd
  * Python
  * InfluxDB (https://github.com/influxdata/influxdb)
  * InfluxDB Python Client (https://github.com/influxdata/influxdb-python)
    - install on linux via 'apt-get install python-influxdb'

## Parameters
  * --interval (in seconds, default: 5)
  * --sabnzbdwebprotocol (http/https, default: http)
  * --sabnzbdhost (default, localhost)
  * --sabnzbdport (default: 8080)
  * --sabnzbdapikey (required, default: empty)
  * --influxdbhost (default: localhost)
  * --influxdbport (default: 8086)
  * --influxdbuser (default: empty)
  * --influxdbpassword (default: empty)
  * --influxdbdatabase (default: plexpy)

## Example

  ```
  python /path/to/sabnzbd_influxdb_export.py --sabnzbdhost <host> --sabnzbdapikey <key>
  ```

## Exported Data
  * Queue
    - # Jobs
    - Total size left (MB)
    - Speed
  * Server Stats
    - Total downloaded
    - Total downloaded (month)
    - Total downloaded (week)
    - Total downloaded (day)
  
### To Do:
  * Coming soon...

## Use-Case (todo: update image)
  With the data exported to influxdb, you can create some useful stats/graphs in graphing tools such as grafana (http://grafana.org/)
  
  ![alt tag](https://cloud.githubusercontent.com/assets/4528753/17122931/7176e2aa-52a5-11e6-8ff1-89ab6a8e7f82.png)
  
  
