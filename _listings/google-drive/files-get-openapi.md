---
swagger: "2.0"
x-collection-name: Google Drive
x-complete: 0
info:
  title: Google Drive Get Files
  description: Lists or searches files.
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
  /changes/startPageToken:
    get:
      summary: Get Start Page Token Changes
      description: Gets the starting pageToken for listing future changes.
      operationId: drive.changes.getStartPageToken
      x-api-path-slug: changesstartpagetoken-get
      parameters:
      - in: query
        name: supportsTeamDrives
        description: Whether the requesting application supports Team Drives
      - in: query
        name: teamDriveId
        description: The ID of the Team Drive for which the starting pageToken for
          listing future changes from that Team Drive will be returned
      responses:
        200:
          description: OK
      tags:
      - Change
  /changes/watch:
    post:
      summary: Watch Changes
      description: Subscribes to changes for a user.
      operationId: drive.changes.watch
      x-api-path-slug: changeswatch-post
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
      - in: body
        name: resource
        schema:
          $ref: '#/definitions/holder'
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
  /channels/stop:
    post:
      summary: Stop Watching Changes
      description: Stop watching resources through this channel
      operationId: drive.channels.stop
      x-api-path-slug: channelsstop-post
      parameters:
      - in: body
        name: resource
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Change
  /files:
    get:
      summary: Get Files
      description: Lists or searches files.
      operationId: drive.files.list
      x-api-path-slug: files-get
      parameters:
      - in: query
        name: corpora
        description: Comma-separated list of bodies of items (files/documents) to
          which the query applies
      - in: query
        name: corpus
        description: The source of files to list
      - in: query
        name: includeTeamDriveItems
        description: Whether Team Drive items should be included in results
      - in: query
        name: orderBy
        description: A comma-separated list of sort keys
      - in: query
        name: pageSize
        description: The maximum number of files to return per page
      - in: query
        name: pageToken
        description: The token for continuing a previous list request on the next
          page
      - in: query
        name: q
        description: A query for filtering the file results
      - in: query
        name: spaces
        description: A comma-separated list of spaces to query within the corpus
      - in: query
        name: supportsTeamDrives
        description: Whether the requesting application supports Team Drives
      - in: query
        name: teamDriveId
        description: ID of Team Drive to search
      responses:
        200:
          description: OK
      tags:
      - File
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