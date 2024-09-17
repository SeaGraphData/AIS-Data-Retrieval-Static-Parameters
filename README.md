# AIS Data Retrieval Tool for Missed Static Parameters using Web Scraping Methodology

The **AIS Vessel Data Retrieval** project consists of a python-based Jupyter-notebook designed for the analysis and visualization of Automatic Identification System (AIS) data, utilizing historical data from the [NOAA AIS Data](https://coast.noaa.gov/htdata/CMSP/AISDataHandler/2020/index.html) historical data. The user can go freely to the website and download them, as it is done in previous repositories. 

The dataset analyzed in this case study pertains to January 1, 2020, and has undergone data cleaning and visualization processes, employing tools such as Folium and other Python libraries (Pandas and Numpy) to explore specific cases.

Since AIS data, which are real-world data, frequently lack particular attribute values or trends and are frequently inconsistent, erroneous (contains mistakes or outliers), and incomplete [1], this project introduces a tool to recover missing or unavailable static AIS data fields, such as vessel name, IMO number, call sign, and other identifying parameters. The motivation behind this approach lies in the mutable nature of the Maritime Mobile Service Identity (MMSI) number, which can change over time. Although the frequency of vessels changing nationality is relatively low compared to the total global fleet (primarily through the second-hand market), reliance on the MMSI alone may yield inaccurate results when identifying vessels. Instead, the International Maritime Organization (IMO) number, a permanent and unique identifier, is preferred for vessel tracking. The proposed method leverages cross-referencing between the MMSI and IMO numbers using external sources of information to enhance data reliability.


To achieve this, we implement web scraping techniques, following the methodology outlined in a previous repository titled [Web Scraping and Vessel Data](https://github.com/SeaGraphData/Web-Scraping-ShipInfo).  This enables cross-validation of the AIS dataset with MMSI-IMO relationships sourced from external databases, facilitating the retrieval of accurate vessel information, such as the IMO number, current vessel name, and, where applicable, vessel type.

For data enrichment,[ShipInfo Website](https://shipinfo.net) is utilized as the primary source. However, alternative resources, such as [Vessel Finder](https://www.vesselfinder.com/vessels), may also be employed, offering additional data on gross tonnage (GT), deadweight tonnage (DWT), and vessel dimensions—crucial for the classification of ships into subcategories (e.g., Supramax, Panamax). Other potential data sources include the  [DNV Register List](https://vesselregister.dnv.com/vesselregister) (although access is contingent upon possessing a vessel-specific DNV number), [Lloyds Register list](https://www.lr.org/en/about-us/who-we-are/lr-ships-in-class/), and the [Q88](https://www.q88.com/ViewShip.aspx?imo=9796975) platform, which provides data on classification societies and ship ownership.

This approach demonstrates a robust framework for overcoming limitations in AIS data, particularly in cases where static parameters are incomplete, thereby enabling more accurate identification and classification of maritime vessels.

## References

[1] Farshad F., Florent N., Fahimeh F., Paavo N., Javad S., Jukka H. and Csaba R.(2023). *A Comprehensive Study of Clustering-Based Techniques for Detecting Abnormal Vessel Behavior*. *. Remote Sens. 2023, 15, 1477. https://doi.org/10.3390/rs15061477

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





