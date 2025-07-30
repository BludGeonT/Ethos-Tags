# Ethos-Tags

#### Ethos-Tags Needs
We need to create a tagging system for items stored in the EthosProject Databases.  For example, Ethos-OCR has a database full of screenshots of spam, scams, hackers, fraud, illegal weapon sales, drugs, etc.  These records contain data that will be used by the EthosProject ecosystem and what will make this very organized an manageable is to create a tagging module where calassifications of data can be assigned to records.  

##### Examples of TAGS:
- ```FRAUD```
- ```WEAPONS```
- ```DRUGS```
- ```CRYPTO```
- ```TRAFFICKING```
- ```SCAM```
- ```TERRORISM```

###### Ethos Tag Descriptions
Each Ethos Tag that is created will have a description of what the Tag should be used for.  This will be prompted to the EthosProject operator upon creating a new tag which will require information about the tag.  

##### User Definable Tags
The interface for the Ethos-Tags will have a UI area for Ethos Operators to manage tags including creating, editing, deleting, and defining them.  We are trying to make EthosProject all comprised of modules to allow for the best flexibility and ease to add and remove any modules that are part of it all.  

##### Ethos-Tags Architecture
This module should be very basic.  Included will be a small database that contains and records all of the tags that will be created.  In it's first iteration and simplest form, we will have TAGNAME and TAG_DESCRIPTION and fields within each record.

- The database should be set up with security so that the other databases in the EthosProject can pull tag information from it.
- Other modules like Ethos-OCR and it's database of records, will need to set tags on its records.  From with the Ethos-OCR interface, and for each record within its database, we should be able to add one or multiple tags to each record.  When someone in Ethos-OCR clicks on "Edit Tags" for a record, an interface will come up and query the Tags database for all defined tags and then build that as a list to choose from. Once the Operator makes the choice or choices of tags on a record from Ethos-OCR, then those tags will be saved in the Ethos-OCR database record.
  - There will likely be other EthosProject modules that will be interfacging with this Ethos-Tags database.
- This Ethos-Tags database will serve Tags to other EthosProject modules and this Ethos-Tags module should have knowledge about all of the other databases within The EthosProject as eventually reports will be created and generated from the Tags module to produce reports on all records across the EthosProject related to tags and specific incidents.

##### Ethos-Tags Audit Logging Trail
As with every EthosProject module, there needs to be audit logging of all actions that have been executed.  Examples are creating new tags, editing a tag, deleting tags, and generating reports.  The EthosProject operator's name will be logged along with their actions inside of EthosProject.
- Care needs to be taken because we will eventually come up with a central logging module for all EthosProject actions being taken where every event will be logged in a standardized output similiar to weblogs from Nginx or IIS.  Eventually we will have a CentralLogging module created which will interface with all of the EthosProject modules so that there is a central utility to go over, analyze, and generate reports on all clicks, actions, and commands given by EthosProject operators.

##### Ethos-Tags User Interface (UI)
- For detailed information on the UI layout and functionality, refer to the ```UI.md``` file in this repository.

  
