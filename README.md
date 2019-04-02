# FSC Exercise

Creating the FSC is File Systems connector is responsible for discovering and indexing local file content with ACLs and index it into Cloud Search. Once successfully indexed, content from the local file is searchable through Search Interface.

There is a Search Interface using for search content from the local file and is located in GAE/local.

### Requirements
- Create a <b>Content Connector</b> to traverse file content on local server
- Create a <b>Content Connector</b> to collect contents on the target database
- Create a <b>Identity Connector</b> to sync identities from UAA server to GCS Identity Source
- Provide a <b>search interface</b> for searching content 
- Create a <b>Springboot GAE application</b> to manage external users and group string on Google Cloud Identiy  
(This connector implements the graph traversal strategy provided by the Content Connector SDK)
- Create <b>WME Java SDK</b> for interacting with WME ecossystem APIs

### List of steps 
- Create a <b>Content Connector</b> to traverse file content on local server 
  + Configuring the connector
  + Listing the content of folders and files
  + Reading permissions (ACLs) for both files and folders
  +	Performing the graph traversal
  + Observing traversal schedules
  + Respecting Access Control Lists (ACLs) 
- Create a <b>Content Connector</b> to collect contents on db (providing later)
  + Configuring the connector
  + Accessing the target database
  + Identifying searchable content
  + Performing traversals
  + Observing traversal schedules
  + Sending SQL queries to the database to retrieve records
  + Respecting Access Control Lists (ACLs)
- Create a <b>Identity Connector</b> to sync identities from omt server to GCS Identity Source
  + Retrieve all users from UAA server and send them to Google for syncing with Google identities.
  + Retrieve all groups from UAA and send them to Google for syncing with Google identities.
- Provide a <b>search interface</b> for searching content
  + Configure a search application 
  + Generate OAuth credentials for the application
  + Handle Login dialog
  + Query the index
  + Display the query results
  + Display the facet results
  + Deploy the UI to GAE
- Create a <b>FSC application</b>
  + Export REST APIs to manage identities and group
  + Provide an Interface to manage Group, External identities, ...
- Create <b>WME Java SDK</b> 
  + Create WME connection by authenticating with providing account
  + Get Memberships for Group

### Architecture
<img src="https://developers.google.com/cloud-search/images/architecture-overview.png?authuser=1"></img>
### 
