## Nosewheelie

Nosewheelie is the api for Citibikes that provides the data that you
would like.

# Why?

At the moment, the citibike service provides a json service that give
the state of the service during the time of the query. This is awesome,
but for those looking for trends or to make a specific set of
visualizations we have a different set of needs.

# What does it provide?

* Historical Data (data within a given date range)
* Retrieval of Data at a Station level for a date range  
* Total Bicycles in the system
* Active Bicycles in the system
* Usage ratio


# How does it work?

Give that we are dealing with data from a given date range. Any request
made without a range will provide data for the current moment (the same
a requesting the data directly from the citibike source directly).

If the data for that date range has aged out of the database or is
unavailable, a 410 is returned.


## Some sample queries

### Data for a given station

` <server address>/station/id`

sample output 

`{
   "id":72,
   "stationName":"W 52 St & 11 Av",
   "availableDocks":16,
   "totalDocks":39,
   "latitude":40.76727216,
   "longitude":-73.99392888,
   "statusValue":"In Service",
   "statusKey":1,
   "availableBikes":17,
   "stAddress1":"W 52 St & 11 Av",
   "stAddress2":"",
   "city":"",
   "postalCode":"",
   "location":"",
   "altitude":"",
   "testStation":false,
   "lastCommunicationTime":null,
   "landMark":""}
`

### Active Bicycles in the system





