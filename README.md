# AIS Data Retrieval Tool for Missed Static Parameters using Web Scraping Methodolog

The **AIS Vessel Data Retrieval** project consists of a python-based Jupyter-notebook 
designed to analyze and Visualize AIS data using the [NOAA AIS Data](https://coast.noaa.gov/htdata/CMSP/AISDataHandler/2020/index.html) historical data. The files are given in csv format and because they are quite big (around 3 GB each), it could not be possible to attach here. However, the user can go freely to the website and download them, as it is done in previous repositories.

The case here shared is based on 1st January 2020 and it has been cleaned and visuaslized specific cases using Folium and others libraries.

This project includes a tool to obtain details they cannot be seen or provided in AIS data when part of the table, mainly the static part (Vessel name - IMO - CallSign - etc) is lost or we have NaN values on it. The inspiring point to create this code is the fact that the MMSI is changeable over time and although the number of vessels which  exchange her nationality is small comparing to the rest of the whole fleet (second hand market most probably), MMSI number cannot be the value to rely on and identify the ship we want to analyze. For this purpose it is better to take a look at IMO number (permanent value).The idea behind is to cross check the MMSI with the IMO associated by means of another source of information. 

For instance, we are going to use the Web Scaping methodology applied in our previous repository called [Web Scraping and Vessel Data](https://github.com/SeaGraphData/Web-Scraping-ShipInfo). Thanks to that, we can cross check the AIS file with the MMSI-IMO relationship found in this website, being useful when it comes to getting the real IMO number, the current ship name and/or the type of vessel if possible. 

We choose [ShipInfo Website](https://shipinfo.net) as a reference to get the information needed, but it could be another one, for example, [Vessel Finder](https://www.vesselfinder.com/vessels) ( here we can extract the GT, DWT and sizs of the ship, crucial parameters to classify vessels in subcategories like bulk carriers such as Supramax, Panamax etc). 

Another source of info could be Class Societies [DNV Register List](https://vesselregister.dnv.com/vesselregister) (unfortunately the website link depends on a DNV number, specific for any vessel, but it can be extracted also), or [Lloyds Register list](https://www.lr.org/en/about-us/who-we-are/lr-ships-in-class/). [Q88](https://www.q88.com/ViewShip.aspx?imo=9796975) website could be a good solution in order to find parameters like the Society of Classification and Shipowner.


For any questions about this repository, please contact me via juan.fernandez.sea@gmail.com

## Authors

* [**Juan Fernandez**](mailto://juan.fernandez.sea@gmail.com) - [Linkedin](https://www.linkedin.com/in/juan-fernandez-martinez/)



## Prerequisites

You will require `Jupyter Notebook` to run this code. We recommend that you install 
the latest [Anaconda Python distribution](https://www.anaconda.com/) for your 
operating system. Anaconda Python distributions include Jupyter Notebook.


This collection supports Python 3.10. Although many options are possible, the 
authors highly recommend that users install the appropriate Anaconda package 
for their operating system. In order to ensure that you have all the required 
dependencies, we recommend that you build a suitable Python environment, as 
discussed below.


## Dependencies

|item|version|licence|package info|
|---|---|---|---|
|python|3.10.13|PSF|https://docs.python.org/3/license.html|
|matplotlib|3.8.3|PSFL|https://matplotlib.org/stable/users/project/license.html|
|pandas|2.2.1|BSD-3|https://pandas.pydata.org|
|numpy|1.3.0|BSD-3|https://numpy.org/doc/stable/index.html|
|folium|0.16.0|MIT|https://pypi.org/project/folium/|
|tqdm|4.64.4|MIT|https://tqdm.github.io|





