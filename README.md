# Kartograph Examples

A set of examples using [Kartograph](http://kartograph.org/).

## Data processing

Setup a virtual environment (instructions are using virtualenvwrapper).

    mkvirtualenv kartograph-example
    workon kartograph-example

Install the python packages (Kartograph.py).

    pip install -r requirements.txt
    
Converting shapefiles to SVG.

    mkdir -p data/mn-county-2010/svg
    cd data/mn-county-2010 && kartograph mn-county-2010.json -o svg/mn-county-2010.svg; cd -;