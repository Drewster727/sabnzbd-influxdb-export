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
    - Status
    - *#* Jobs
    - Total size left (MB)
    - Speed
  * Server Stats
    - Total downloaded
    - Total downloaded (month)
    - Total downloaded (week)
    - Total downloaded (day)
  
### To Do:
  * Coming soon...

## Use-Case
  With the data exported to influxdb, you can create some useful stats/graphs in graphing tools such as grafana (http://grafana.org/)
  
  ![alt tag](https://user-images.githubusercontent.com/4528753/29847166-e912f8ec-8cdf-11e7-8dc0-7155435130f6.png)
  
  
