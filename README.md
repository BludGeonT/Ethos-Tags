# Ethos-Tags

#### Ethos-Tags Needs
We need to create a tagging system for items stored in the EthosProject Databases.  For example, Ethos-OCR has a database full of screenshots of spam, scams, hackers, fraud, illegal weapon sales, drugs, etc.  These records contain data that will be used by the EthosProject ecosystem and what will make this very organized an manageable is to create a tagging module where calassifications of data can be assigned to records.  

##### Some examples of TAGS will be:
- ```FRAUD```
- ```WEAPONS```
- ```DRUGS```
- ```CRYPTO```
- ```TRAFFICKING```
- ```SCAM```
- ```TERRORISM```

##### User Definable Tags
The interface for the Ethos-Tags will have a UI area for Ethos Operators to manage tags including creating, editing, deleting, and defining them.  We are trying to make EthosProject all comprised of modules to allow for the best flexibility and ease to add and remove any modules that are part of it all.  

##### Ethos-Tags Architecture
This module should be very basic.  Included will be a small database that contains and records all of the tags that will be created.  In it's first iteration and simplest form, we will have TAGNAME and TAG_DESCRIPTION and fields within each record.

- The database should be set up with security so that the other databases in the EthosProject can pull tag information from it.
- Other modules like Ethos-OCR and it's database of records, will need to set tags on its records.  From with the Ethos-OCR interface, and for each record within its database, we should be able to add one or multiple tags to each record.  When someone in Ethos-OCR clicks on "Edit Tags" for a record, an interface will come up and query the Tags database for all defined tags and then build that as a list to choose from. Once the Operator makes the choice or choices of tags on a record from Ethos-OCR, then those tags will be saved in the Ethos-OCR database record.
