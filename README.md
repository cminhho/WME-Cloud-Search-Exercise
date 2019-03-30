# gcs-exercise

Creating the FSC is File Systems connector is responsible for discovering and indexing local file content with ACLs and index it into Cloud Search. Once successfully indexed, content from the local file is searchable through Search Interface.

There is a Search Interface using for search content from the local file and is located in GAE/local.

### Requirements
- Create a Content Connector to traverse file content on local server (This connector implements the graph traversal strategy provided by the Content Connector SDK)
- Create a Content Connector to collect contents on db (providing later)
- Create a Identity Connector to sync identities from omt server to GCS Identity Source
- Provide a search interface for searching results 
- Create a GAE application

### Task
- Create a Content Connector to traverse file content on local server 
  + List the content of folders
  + Read the content of documents
  + Read attributes of files and folders
  + Read permissions (ACLs) for both files and folders
- Create a Content Connector to collect contents on db (providing later)
  + Accessing the target database
  + Identifying searchable content
  + Performing traversals
  + Observing traversal schedules
  + Sending SQL queries to the database to retrieve records
  + Respecting Access Control Lists (ACLs)
- Create a Identity Connector to sync identities from omt server to GCS Identity Source
  + Retrieve all users from local identity system and send them to Google for syncing with Google identities.
  + Retrieve all groups from local identity system and send them to Google for syncing with Google identities.
- Provide a search interface for searching results 
- Create a GAE application
  + Export REST APIs to manage identities and group
  + A Interface to manage Group, External identities, ...
