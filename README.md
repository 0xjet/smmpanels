# SMM Panels Datasets


## Description
This repository contains the dataset described in the paper:

* D. Nevado-Catalan, S. Pastrana, N. Vallina-Rodiguez, J. Tapiador, and J. Caballero. "An Analysis of Fake Social Media Engagement Services." _Computers & Security_, To appear. [[link](tbd)]

There are 2 versions of the dataset:
 1. `raw_panels_dataset` An unprocessed version that resulted of the crawiling of the panels.
 2. `panels_dataset` A processed version of the previous dataset with extra fields for easier analysis.

## Dataset

Both datasets have the same structure.
Each of them has 58 directories with the name of the an SMMPanel. In every panel
directory there is one `.csv` file per day with available data (some days
the panels were down and therefore no data could be gathered).

### Unprocessed version fields

 - `index`: Row number.
 - `ID`: Unique ID of the service.
 - `Service`: Service name.
 - `Price/1000`: Price per 1000 units in USD.
 - `Min`: Minimum ammount a user is allowed to request.
 - `Max`: Maximum ammount a user is allowed to request.
 - `Description`: Description of the service. This field often details extra
charactersitics of the service like origin or duration.



### Processed version fields

 - `ID`: Unique ID of the service.
 - `Site`: Target platform (i.e. Facebook, Instagram, etc.)
 - `Product`: Offered product (i.e. Likes, Followers, Views, etc.)
 - `Price/1000`: Price per 1000 units in USD.
 - `Min`: Minimum ammount a user is allowed to request.
 - `Max`: Maximum ammount a user is allowed to request.

 The following fields are boolean and indicate the presence of the field's name as a keyword in the service name or description:
 - `Active`.
 - `Real`.
 - `Bot`.
 - `No Drip`.
 - `Drip`.
 - `Non-drip`.
 - `No Drop`.
 - `Drop`.
 - `Non-drop`.
 - `Random`.
 - `Custom`.
 - `No Refill`.
 - `Refill`.
 - `Non-refill`.
 - `Female`.
 - `Male`.
 - `Power`.
 - `HQ`.
 - `LQ`.
 - `No Guarantee`.
 - `Guarantee`.
 - `Refund`.
 - `No refund`.
 - `Non-refund`.
 - `Slow`.
 - `Fast`.
 - `Instant`.
 - `Day`.
 - `Hour`.
 - `Bundle`.

 The following fields are not boolean but have also been derived by searching for keywords in the service name and description.
 - `Geo`: Country of origin of the service.
 - `From`: Only for website traffic. Website placed in the refer field of request heder.
 - `Service`: Service name as it appeared in the original panel.
