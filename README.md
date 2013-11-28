reverse_geocoding_nominatim
===========================

Quick hack to perform reverse geocoding on the Nominatim map database using longitude and latitude.  Currently only pulls address information (street name, zip code, city, neighborhood) but could easily be updated to pull other info as well (country, country_code, state, and county).  

Also currently switches automatically between the OSM hosted nominatim database (http://nominatim.openstreetmap.org/) and the MapQuest hosted nominatim database (http://open.mapquestapi.com/nominatim/v1/).  Switching is performed when one times out or when a threshold is hit, to avoid overloading either of the servers.

To run from command line use:
$ python get_address.py <input_file> <output_file> <log_file> <email_address> [start_line] [end_line] [throttle_time] [delimiter]

REQUIRES: PANDAS
