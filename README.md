# Rail-Stations-API
An API integration to download freight and passenger rail station data for programming and planning use

## Why This Project

Part of the NJTPA's grants reporting process also requires monitoring grants awarded to various rail stations that form the freight and passenger transportation corridor of the NJTPA's subregions, notably high-traffic lines such as the Northeast Corridor. This API-integration pipeline automates a manual process in annotating and collating data on stations by County as the organization looks to oversee all development across its subregions. The result is a replicable pipeline which downloads datasets relating to transit stations, normalizes them into a table and stores it in a database for future reference and complex joins involving programming information for any metropolitan planning organization, or engineering firm.

## Installation Specifics

Pandas and Requests are required as libraries, state-wise data is required. This project connects to the ArcGIS dataset of NJ Passenger Rail Stations available through the New Jersey OpenData Portal. The information is integrated first as a JSON file, which is then converted into a normal table using an ETL function. Sqlite3 is leveraged as a database option, wherein the converted table of rail station records is then stored.

Google Colab was used to minimize exposure of any proprietary tooling or records, with critical project information entirely avoided and its privacy secured. It also enables loading this project into a public repository for feedback and open-source discussions.

## Edge Cases/Debugging

Depending on the constraints, the table may need additional processing as it captures both NJ Transit and Amtrak stations, alongside NYS and Port Authority administered rail stations. During initialization, the extract function had to be reworked a few times to ensure all data was first converted correctly from JSON to a DataFrame. The properties.COUNTY column was used as the record to aggregate and count stations.

## Contributing

All users are welcome to add issues and send pull requests. This is a maiden approach to automating station data for a common processing task among capital programming and rail management professionals working in transportation.

## Authors/Acknowledgement

This project was made possible by the State of NJ's Open Data Portal and Google Colab.
