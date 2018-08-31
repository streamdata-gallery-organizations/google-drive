---
swagger: "2.0"
x-collection-name: Google Drive
x-complete: 0
info:
  title: Google Drive Create File Comment Reply
  description: Creates a new reply to a comment.
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
    post:
      summary: Create File
      description: Creates a new file.
      operationId: drive.files.create
      x-api-path-slug: files-post
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      - in: query
        name: ignoreDefaultVisibility
        description: Whether to ignore the domains default visibility settings for
          the created file
      - in: query
        name: keepRevisionForever
        description: Whether to set the keepForever field in the new head revision
      - in: query
        name: ocrLanguage
        description: A language hint for OCR processing during image import (ISO 639-1
          code)
      - in: query
        name: supportsTeamDrives
        description: Whether the requesting application supports Team Drives
      - in: query
        name: useContentAsIndexableText
        description: Whether to use the uploaded content as indexable text
      responses:
        200:
          description: OK
      tags:
      - File
  /files/generateIds:
    get:
      summary: Generate File IDs
      description: Generates a set of file IDs which can be provided in create requests.
      operationId: drive.files.generateIds
      x-api-path-slug: filesgenerateids-get
      parameters:
      - in: query
        name: count
        description: The number of IDs to return
      - in: query
        name: space
        description: The space in which the IDs can be used to create new files
      responses:
        200:
          description: OK
      tags:
      - File
  /files/trash:
    delete:
      summary: Empty Trash
      description: Permanently deletes all of the user's trashed files.
      operationId: drive.files.emptyTrash
      x-api-path-slug: filestrash-delete
      responses:
        200:
          description: OK
      tags:
      - File
  /files/{fileId}:
    delete:
      summary: Delete File
      description: Permanently deletes a file owned by the user without moving it
        to the trash. If the file belongs to a Team Drive the user must be an organizer
        on the parent. If the target is a folder, all descendants owned by the user
        are also deleted.
      operationId: drive.files.delete
      x-api-path-slug: filesfileid-delete
      parameters:
      - in: path
        name: fileId
        description: The ID of the file
      - in: query
        name: supportsTeamDrives
        description: Whether the requesting application supports Team Drives
      responses:
        200:
          description: OK
      tags:
      - File
    get:
      summary: Get File
      description: Gets a file's metadata or content by ID.
      operationId: drive.files.get
      x-api-path-slug: filesfileid-get
      parameters:
      - in: query
        name: acknowledgeAbuse
        description: Whether the user is acknowledging the risk of downloading known
          malware or other abusive files
      - in: path
        name: fileId
        description: The ID of the file
      - in: query
        name: supportsTeamDrives
        description: Whether the requesting application supports Team Drives
      responses:
        200:
          description: OK
      tags:
      - File
    patch:
      summary: Update File
      description: Updates a file's metadata and/or content with patch semantics.
      operationId: drive.files.update
      x-api-path-slug: filesfileid-patch
      parameters:
      - in: query
        name: addParents
        description: A comma-separated list of parent IDs to add
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: fileId
        description: The ID of the file
      - in: query
        name: keepRevisionForever
        description: Whether to set the keepForever field in the new head revision
      - in: query
        name: ocrLanguage
        description: A language hint for OCR processing during image import (ISO 639-1
          code)
      - in: query
        name: removeParents
        description: A comma-separated list of parent IDs to remove
      - in: query
        name: supportsTeamDrives
        description: Whether the requesting application supports Team Drives
      - in: query
        name: useContentAsIndexableText
        description: Whether to use the uploaded content as indexable text
      responses:
        200:
          description: OK
      tags:
      - File
  /files/{fileId}/comments:
    get:
      summary: Get File Comments
      description: Lists a file's comments.
      operationId: drive.comments.list
      x-api-path-slug: filesfileidcomments-get
      parameters:
      - in: path
        name: fileId
        description: The ID of the file
      - in: query
        name: includeDeleted
        description: Whether to include deleted comments
      - in: query
        name: pageSize
        description: The maximum number of comments to return per page
      - in: query
        name: pageToken
        description: The token for continuing a previous list request on the next
          page
      - in: query
        name: startModifiedTime
        description: The minimum value of modifiedTime for the result comments (RFC
          3339 date-time)
      responses:
        200:
          description: OK
      tags:
      - Comment
    post:
      summary: Create File Comment
      description: Creates a new comment on a file.
      operationId: drive.comments.create
      x-api-path-slug: filesfileidcomments-post
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: fileId
        description: The ID of the file
      responses:
        200:
          description: OK
      tags:
      - Comment
  /files/{fileId}/comments/{commentId}:
    delete:
      summary: Delete File Comment
      description: Deletes a comment.
      operationId: drive.comments.delete
      x-api-path-slug: filesfileidcommentscommentid-delete
      parameters:
      - in: path
        name: commentId
        description: The ID of the comment
      - in: path
        name: fileId
        description: The ID of the file
      responses:
        200:
          description: OK
      tags:
      - Comment
    get:
      summary: Get File Comment
      description: Gets a comment by ID.
      operationId: drive.comments.get
      x-api-path-slug: filesfileidcommentscommentid-get
      parameters:
      - in: path
        name: commentId
        description: The ID of the comment
      - in: path
        name: fileId
        description: The ID of the file
      - in: query
        name: includeDeleted
        description: Whether to return deleted comments
      responses:
        200:
          description: OK
      tags:
      - Comment
    patch:
      summary: Update File Comment
      description: Updates a comment with patch semantics.
      operationId: drive.comments.update
      x-api-path-slug: filesfileidcommentscommentid-patch
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: commentId
        description: The ID of the comment
      - in: path
        name: fileId
        description: The ID of the file
      responses:
        200:
          description: OK
      tags:
      - Comment
  /files/{fileId}/comments/{commentId}/replies:
    get:
      summary: Get File Comment Replies
      description: Lists a comment's replies.
      operationId: drive.replies.list
      x-api-path-slug: filesfileidcommentscommentidreplies-get
      parameters:
      - in: path
        name: commentId
        description: The ID of the comment
      - in: path
        name: fileId
        description: The ID of the file
      - in: query
        name: includeDeleted
        description: Whether to include deleted replies
      - in: query
        name: pageSize
        description: The maximum number of replies to return per page
      - in: query
        name: pageToken
        description: The token for continuing a previous list request on the next
          page
      responses:
        200:
          description: OK
      tags:
      - Comment
    post:
      summary: Create File Comment Reply
      description: Creates a new reply to a comment.
      operationId: drive.replies.create
      x-api-path-slug: filesfileidcommentscommentidreplies-post
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: commentId
        description: The ID of the comment
      - in: path
        name: fileId
        description: The ID of the file
      responses:
        200:
          description: OK
      tags:
      - Comment
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