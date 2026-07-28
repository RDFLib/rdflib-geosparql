# rdflib-geosparql
An implementation of the GeoSPARQL standard's functions for use with RDFlib Graphs

## Capabilities

The library implements the following functions:

* GeoSPARQL 1.0 and GeoSPARQL 1.1 Functions using the official namespace geof: http://www.opengis.net/def/function/geosparql/
* Further geospatial functions which have not yet been standardized in GeoSPARQL under the namespace geofe:http://www.opengis.net/def/function/geosparql/ext/

URIs of standardized GeoSPARQL functions will not change.
URIs of non-standardized functions might change in the case that these functions become standardized and assigned a new URI.

## Jupyter Notebooks as Tutorials

This repository includes the following Jupyter Notebooks which showcase the implemented query functions on the given [testdataset](tests/testdata.ttl).

* [GeoSPARQL 1.0 Functions](GeoSPARQL10.ipynb)
* [GeoSPARQL 1.1 Functions](GeoSPARQL11.ipynb)
* [GeoSPARQL Ext Functions](GeoSPARQLExt.ipynb)

The query functions in these Jupyter Notebooks are almost exclusively operating on WKT Literals.
For a more comprehensive test please refer to the Python test classes in the [tests folder](tests).

While the Jupyter Notebooks are automatically rendered in Github, not all features of the Jupyter Notebooks are available in the GitHub rendering (e.g. Leaflet Map Views).
To make use of these visualizations, please clone the repository and execute the Jupyter Notebook in your preferred Jupyter Notebook environment.
 
### Literal Types

rdflib-geosparql supports the following geospatial literal types:

* DGGS Literal (GeoSPARQL 1.1)
* GML Literal (GeoSPARQL 1.0)
* KML Literal (GeoSPARQL 1.1)
* GeoJSON Literal (GeoSPARQL 1.1)
* GLTF Literal (GeoSPARQL Ext)
* JSONFG Literal (GeoSPARQL Ext)
* PLY Literal (GeoSPARQL Ext)
* Well-Known Text Literal (GeoSPARQL 1.0)

The DGGS Literal is able to support a variety of DGGS systems.
rdflib-geosparql only supports a subset of DGGS systems, but support may be expanded in the future

## Installation

To run the tests or Jupyter notebooks, install this library like this:

1. Create a Python 3.12 Virtual Environment
    * e.g. using an installed version of Python 3.12 and then running `python3.12 -m venv .venv` on the command line
2. Activate the created Virtual Environment
   * `source .venv/bin/activate`
3. Install requirements
    * `pip install -r requirements.txt`

After installation, you should run the test to ensure everything is working:

4. Run tests
    * `pytest`

## Documentation

Documentation for this library is made using [Doxygen](https://www.doxygen.nl/) which reads the contents of `docs/` and comments and other elements of the code files in `geosparql/` and builds a series of HTML web pages.

To build the documentation:

1. install Doxygen
    a. on a Mac, this is something like `brew install doxygen graphviz
    b. on Ubuntu Linux, this is something like `sudo apt update && sudo apt install doxygen`
2. build the documentation
    a. within the `docs/` folder, run the command `doxygen Doxyfile`
    b. this will produce a folder called `html/` within docs and the starting page is `index.html`
