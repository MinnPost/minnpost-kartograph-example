# Kartograph Examples

A set of examples using [Kartograph](http://kartograph.org/).

## Data processing

Setup a virtual environment (instructions are using virtualenvwrapper).

    mkvirtualenv kartograph-example
    workon kartograph-example

Install the python packages (Kartograph.py).

    pip install -r requirements.txt
    
### Converting shapefiles to SVG

For counties.  We need to convert to 4326 (lat/lon) as Kartograph.py seems to like that.  (We used [MapShaper](http://mapshaper.com/test/MapShaper.swf) to simplify shapes a bit)

    ogr2ogr -t_srs EPSG:4326 data/mn-county-2010/shp-dp-60-proj-4326/county2010.shp data/mn-county-2010/shp-dp-60/county2010.shp
    cd data/mn-county-2010 && kartograph mn-county-2010.json -o svg/mn-county-2010-dp-60.svg; cd -;
    