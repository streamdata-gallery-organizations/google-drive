---
swagger: "2.0"
x-collection-name: Google Drive
x-complete: 0
info:
  title: Google Drive Get Changes
  description: Lists the changes for a user or Team Drive.
  termsOfService: https://developers.google.com/terms/
  contact:
    name: Google
    url: https://google.com
  version: v3
host: www.googleapis.com
basePath: /drive/v3
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /about:
    get:
      summary: Get About
      description: Gets information about the user, the user's Drive, and system capabilities.
      operationId: drive.about.get
      x-api-path-slug: about-get
      responses:
        200:
          description: OK
      tags:
      - About
  /changes:
    get:
      summary: Get Changes
      description: Lists the changes for a user or Team Drive.
      operationId: drive.changes.list
      x-api-path-slug: changes-get
      parameters:
      - in: query
        name: includeCorpusRemovals
        description: Whether changes should include the file resource if the file
          is still accessible by the user at the time of the request, even when a
          file was removed from the list of changes and there will be no further change
          entries for this file
      - in: query
        name: includeRemoved
        description: Whether to include changes indicating that items have been removed
          from the list of changes, for example by deletion or loss of access
      - in: query
        name: includeTeamDriveItems
        description: Whether Team Drive files or changes should be included in results
      - in: query
        name: pageSize
        description: The maximum number of changes to return per page
      - in: query
        name: pageToken
        description: The token for continuing a previous list request on the next
          page
      - in: query
        name: restrictToMyDrive
        description: Whether to restrict the results to changes inside the My Drive
          hierarchy
      - in: query
        name: spaces
        description: A comma-separated list of spaces to query within the user corpus
      - in: query
        name: supportsTeamDrives
        description: Whether the requesting application supports Team Drives
      - in: query
        name: teamDriveId
        description: The Team Drive from which changes will be returned
      responses:
        200:
          description: OK
      tags:
      - Change
x-streamrank:
  polling_total_time_average: 0
  polling_size_download_average: 0
  streaming_total_time_average: 0
  streaming_size_download_average: 0
  change_yes: 0
  change_no: 0
  time_percentage: 0
  size_percentage: 0
  change_percentage: 0
  last_run: ""
  days_run: 0
  minute_run: 0
---