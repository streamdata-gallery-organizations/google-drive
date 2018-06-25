---
name: Google Drive
x-slug: google-drive
description: Google Drive is a file storage and synchronization service operated by
  Google. It allows users to store files in the cloud, synchronize files across devices,
  and share files. Google Drive encompasses Google Docs, Sheets and Slides, an office
  suite that permits collaborative editing of documents, spreadsheets, presentations,
  drawings, forms, and more.
image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-drive-logo-new.png
x-kinRank: "9"
x-alexaRank: "0"
tags: Google Drive
created: "2018-06-25"
modified: "2018-06-25"
url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-drive/master/_listings/google-drive/apis.md
specificationVersion: "0.14"
apis:
- name: Google Drive Get About
  x-api-slug: google-drive
  description: Gets information about the user, the user's Drive, and system capabilities.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-drive-logo-new.png
  humanURL: https://developers.google.com/drive/
  baseURL: https://www.googleapis.com//drive/v3//about
  tags: About
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-drive/master/_listings/google-drive/about-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-drive/master/_listings/google-drive/about-get-openapi.md
- name: Google Drive Get Changes
  x-api-slug: google-drive
  description: Lists the changes for a user or Team Drive.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-drive-logo-new.png
  humanURL: https://developers.google.com/drive/
  baseURL: https://www.googleapis.com//drive/v3//changes
  tags: Change
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-drive/master/_listings/google-drive/changes-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-drive/master/_listings/google-drive/changes-get-openapi.md
- name: Google Drive Get Start Page Token Changes
  x-api-slug: google-drive
  description: Gets the starting pageToken for listing future changes.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-drive-logo-new.png
  humanURL: https://developers.google.com/drive/
  baseURL: https://www.googleapis.com//drive/v3//changes/startPageToken
  tags: Change
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-drive/master/_listings/google-drive/changesstartpagetoken-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-drive/master/_listings/google-drive/changesstartpagetoken-get-openapi.md
- name: Google Drive Watch Changes
  x-api-slug: google-drive
  description: Subscribes to changes for a user.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-drive-logo-new.png
  humanURL: https://developers.google.com/drive/
  baseURL: https://www.googleapis.com//drive/v3//changes/watch
  tags: Change
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-drive/master/_listings/google-drive/changeswatch-post-openapi.md
- name: Google Drive Stop Watching Changes
  x-api-slug: google-drive
  description: Stop watching resources through this channel
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-drive-logo-new.png
  humanURL: https://developers.google.com/drive/
  baseURL: https://www.googleapis.com//drive/v3//channels/stop
  tags: Change
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-drive/master/_listings/google-drive/channelsstop-post-openapi.md
- name: Google Drive Get Files
  x-api-slug: google-drive
  description: Lists or searches files.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-drive-logo-new.png
  humanURL: https://developers.google.com/drive/
  baseURL: https://www.googleapis.com//drive/v3//files
  tags: File
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-drive/master/_listings/google-drive/files-get-openapi.md
- name: Google Drive Create File
  x-api-slug: google-drive
  description: Creates a new file.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-drive-logo-new.png
  humanURL: https://developers.google.com/drive/
  baseURL: https://www.googleapis.com//drive/v3//files
  tags: File
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-drive/master/_listings/google-drive/files-post-openapi.md
- name: Google Drive Generate File IDs
  x-api-slug: google-drive
  description: Generates a set of file IDs which can be provided in create requests.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-drive-logo-new.png
  humanURL: https://developers.google.com/drive/
  baseURL: https://www.googleapis.com//drive/v3//files/generateIds
  tags: File
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-drive/master/_listings/google-drive/filesgenerateids-get-openapi.md
- name: Google Drive Empty Trash
  x-api-slug: google-drive
  description: Permanently deletes all of the user's trashed files.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-drive-logo-new.png
  humanURL: https://developers.google.com/drive/
  baseURL: https://www.googleapis.com//drive/v3//files/trash
  tags: File
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-drive/master/_listings/google-drive/filestrash-delete-openapi.md
- name: Google Drive Delete File
  x-api-slug: google-drive
  description: Permanently deletes a file owned by the user without moving it to the
    trash. If the file belongs to a Team Drive the user must be an organizer on the
    parent. If the target is a folder, all descendants owned by the user are also
    deleted.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-drive-logo-new.png
  humanURL: https://developers.google.com/drive/
  baseURL: https://www.googleapis.com//drive/v3//files/{fileId}
  tags: File
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-drive/master/_listings/google-drive/filesfileid-delete-openapi.md
- name: Google Drive Get File
  x-api-slug: google-drive
  description: Gets a file's metadata or content by ID.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-drive-logo-new.png
  humanURL: https://developers.google.com/drive/
  baseURL: https://www.googleapis.com//drive/v3//files/{fileId}
  tags: File
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-drive/master/_listings/google-drive/filesfileid-get-openapi.md
- name: Google Drive Update File
  x-api-slug: google-drive
  description: Updates a file's metadata and/or content with patch semantics.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-drive-logo-new.png
  humanURL: https://developers.google.com/drive/
  baseURL: https://www.googleapis.com//drive/v3//files/{fileId}
  tags: File
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-drive/master/_listings/google-drive/filesfileid-patch-openapi.md
- name: Google Drive Get File Comments
  x-api-slug: google-drive
  description: Lists a file's comments.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-drive-logo-new.png
  humanURL: https://developers.google.com/drive/
  baseURL: https://www.googleapis.com//drive/v3//files/{fileId}/comments
  tags: Comment
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-drive/master/_listings/google-drive/filesfileidcomments-get-openapi.md
- name: Google Drive Create File Comment
  x-api-slug: google-drive
  description: Creates a new comment on a file.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-drive-logo-new.png
  humanURL: https://developers.google.com/drive/
  baseURL: https://www.googleapis.com//drive/v3//files/{fileId}/comments
  tags: Comment
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-drive/master/_listings/google-drive/filesfileidcomments-post-openapi.md
- name: Google Drive Delete File Comment
  x-api-slug: google-drive
  description: Deletes a comment.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-drive-logo-new.png
  humanURL: https://developers.google.com/drive/
  baseURL: https://www.googleapis.com//drive/v3//files/{fileId}/comments/{commentId}
  tags: Comment
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-drive/master/_listings/google-drive/filesfileidcommentscommentid-delete-openapi.md
- name: Google Drive Get File Comment
  x-api-slug: google-drive
  description: Gets a comment by ID.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-drive-logo-new.png
  humanURL: https://developers.google.com/drive/
  baseURL: https://www.googleapis.com//drive/v3//files/{fileId}/comments/{commentId}
  tags: Comment
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-drive/master/_listings/google-drive/filesfileidcommentscommentid-get-openapi.md
- name: Google Drive Update File Comment
  x-api-slug: google-drive
  description: Updates a comment with patch semantics.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-drive-logo-new.png
  humanURL: https://developers.google.com/drive/
  baseURL: https://www.googleapis.com//drive/v3//files/{fileId}/comments/{commentId}
  tags: Comment
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-drive/master/_listings/google-drive/filesfileidcommentscommentid-patch-openapi.md
- name: Google Drive Get File Comment Replies
  x-api-slug: google-drive
  description: Lists a comment's replies.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-drive-logo-new.png
  humanURL: https://developers.google.com/drive/
  baseURL: https://www.googleapis.com//drive/v3//files/{fileId}/comments/{commentId}/replies
  tags: Comment
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-drive/master/_listings/google-drive/filesfileidcommentscommentidreplies-get-openapi.md
- name: Google Drive Create File Comment Reply
  x-api-slug: google-drive
  description: Creates a new reply to a comment.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-drive-logo-new.png
  humanURL: https://developers.google.com/drive/
  baseURL: https://www.googleapis.com//drive/v3//files/{fileId}/comments/{commentId}/replies
  tags: Comment
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-drive/master/_listings/google-drive/filesfileidcommentscommentidreplies-post-openapi.md
- name: Google Drive Delete File Comment Reply
  x-api-slug: google-drive
  description: Deletes a reply.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-drive-logo-new.png
  humanURL: https://developers.google.com/drive/
  baseURL: https://www.googleapis.com//drive/v3//files/{fileId}/comments/{commentId}/replies/{replyId}
  tags: Comment
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-drive/master/_listings/google-drive/filesfileidcommentscommentidrepliesreplyid-delete-openapi.md
- name: Google Drive Get File Comment Reply
  x-api-slug: google-drive
  description: Gets a reply by ID.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-drive-logo-new.png
  humanURL: https://developers.google.com/drive/
  baseURL: https://www.googleapis.com//drive/v3//files/{fileId}/comments/{commentId}/replies/{replyId}
  tags: Comment
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-drive/master/_listings/google-drive/filesfileidcommentscommentidrepliesreplyid-get-openapi.md
- name: Google Drive Update File Comment Reply
  x-api-slug: google-drive
  description: Updates a reply with patch semantics.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-drive-logo-new.png
  humanURL: https://developers.google.com/drive/
  baseURL: https://www.googleapis.com//drive/v3//files/{fileId}/comments/{commentId}/replies/{replyId}
  tags: Comment
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-drive/master/_listings/google-drive/filesfileidcommentscommentidrepliesreplyid-patch-openapi.md
- name: Google Drive Copy File
  x-api-slug: google-drive
  description: Creates a copy of a file and applies any requested updates with patch
    semantics.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-drive-logo-new.png
  humanURL: https://developers.google.com/drive/
  baseURL: https://www.googleapis.com//drive/v3//files/{fileId}/copy
  tags: File
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-drive/master/_listings/google-drive/filesfileidcopy-post-openapi.md
- name: Google Drive Export File
  x-api-slug: google-drive
  description: Exports a Google Doc to the requested MIME type and returns the exported
    content.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-drive-logo-new.png
  humanURL: https://developers.google.com/drive/
  baseURL: https://www.googleapis.com//drive/v3//files/{fileId}/export
  tags: File
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-drive/master/_listings/google-drive/filesfileidexport-get-openapi.md
- name: Google Drive Get File Permissions
  x-api-slug: google-drive
  description: Lists a file's or Team Drive's permissions.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-drive-logo-new.png
  humanURL: https://developers.google.com/drive/
  baseURL: https://www.googleapis.com//drive/v3//files/{fileId}/permissions
  tags: Permission
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-drive/master/_listings/google-drive/filesfileidpermissions-get-openapi.md
- name: Google Drive Create File Permission
  x-api-slug: google-drive
  description: Creates a permission for a file or Team Drive.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-drive-logo-new.png
  humanURL: https://developers.google.com/drive/
  baseURL: https://www.googleapis.com//drive/v3//files/{fileId}/permissions
  tags: Permission
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-drive/master/_listings/google-drive/filesfileidpermissions-post-openapi.md
- name: Google Drive Delete File Permission
  x-api-slug: google-drive
  description: Deletes a permission.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-drive-logo-new.png
  humanURL: https://developers.google.com/drive/
  baseURL: https://www.googleapis.com//drive/v3//files/{fileId}/permissions/{permissionId}
  tags: Permission
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-drive/master/_listings/google-drive/filesfileidpermissionspermissionid-delete-openapi.md
- name: Google Drive Get File Permission
  x-api-slug: google-drive
  description: Gets a permission by ID.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-drive-logo-new.png
  humanURL: https://developers.google.com/drive/
  baseURL: https://www.googleapis.com//drive/v3//files/{fileId}/permissions/{permissionId}
  tags: Permission
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-drive/master/_listings/google-drive/filesfileidpermissionspermissionid-get-openapi.md
- name: Google Drive Update File Permission
  x-api-slug: google-drive
  description: Updates a permission with patch semantics.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-drive-logo-new.png
  humanURL: https://developers.google.com/drive/
  baseURL: https://www.googleapis.com//drive/v3//files/{fileId}/permissions/{permissionId}
  tags: Permission
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-drive/master/_listings/google-drive/filesfileidpermissionspermissionid-patch-openapi.md
- name: Google Drive Get File Revisions
  x-api-slug: google-drive
  description: Lists a file's revisions.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-drive-logo-new.png
  humanURL: https://developers.google.com/drive/
  baseURL: https://www.googleapis.com//drive/v3//files/{fileId}/revisions
  tags: Revision
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-drive/master/_listings/google-drive/filesfileidrevisions-get-openapi.md
- name: Google Drive Delete File Revision
  x-api-slug: google-drive
  description: Permanently deletes a revision. This method is only applicable to files
    with binary content in Drive.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-drive-logo-new.png
  humanURL: https://developers.google.com/drive/
  baseURL: https://www.googleapis.com//drive/v3//files/{fileId}/revisions/{revisionId}
  tags: Revision
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-drive/master/_listings/google-drive/filesfileidrevisionsrevisionid-delete-openapi.md
- name: Google Drive Get File Revision
  x-api-slug: google-drive
  description: Gets a revision's metadata or content by ID.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-drive-logo-new.png
  humanURL: https://developers.google.com/drive/
  baseURL: https://www.googleapis.com//drive/v3//files/{fileId}/revisions/{revisionId}
  tags: Revision
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-drive/master/_listings/google-drive/filesfileidrevisionsrevisionid-get-openapi.md
- name: Google Drive Update File Revision
  x-api-slug: google-drive
  description: Updates a revision with patch semantics.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-drive-logo-new.png
  humanURL: https://developers.google.com/drive/
  baseURL: https://www.googleapis.com//drive/v3//files/{fileId}/revisions/{revisionId}
  tags: Revision
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-drive/master/_listings/google-drive/filesfileidrevisionsrevisionid-patch-openapi.md
- name: Google Drive Watch File
  x-api-slug: google-drive
  description: Subscribes to changes to a file
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-drive-logo-new.png
  humanURL: https://developers.google.com/drive/
  baseURL: https://www.googleapis.com//drive/v3//files/{fileId}/watch
  tags: File
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-drive/master/_listings/google-drive/filesfileidwatch-post-openapi.md
- name: Google Drive Get Team Drives
  x-api-slug: google-drive
  description: Lists the user's Team Drives.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-drive-logo-new.png
  humanURL: https://developers.google.com/drive/
  baseURL: https://www.googleapis.com//drive/v3//teamdrives
  tags: Team Drive
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-drive/master/_listings/google-drive/teamdrives-get-openapi.md
- name: Google Drive Create Team Drive
  x-api-slug: google-drive
  description: Creates a new Team Drive.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-drive-logo-new.png
  humanURL: https://developers.google.com/drive/
  baseURL: https://www.googleapis.com//drive/v3//teamdrives
  tags: Team Drive
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-drive/master/_listings/google-drive/teamdrives-post-openapi.md
- name: Google Drive Delete Team Drive
  x-api-slug: google-drive
  description: Permanently deletes a Team Drive for which the user is an organizer.
    The Team Drive cannot contain any untrashed items.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-drive-logo-new.png
  humanURL: https://developers.google.com/drive/
  baseURL: https://www.googleapis.com//drive/v3//teamdrives/{teamDriveId}
  tags: Team Drive
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-drive/master/_listings/google-drive/teamdrivesteamdriveid-delete-openapi.md
- name: Google Drive CrGeteate Team Drive
  x-api-slug: google-drive
  description: Gets a Team Drive's metadata by ID.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-drive-logo-new.png
  humanURL: https://developers.google.com/drive/
  baseURL: https://www.googleapis.com//drive/v3//teamdrives/{teamDriveId}
  tags: Team Drive
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-drive/master/_listings/google-drive/teamdrivesteamdriveid-get-openapi.md
- name: Google Drive Update Team Drive
  x-api-slug: google-drive
  description: Updates a Team Drive's metadata
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-drive-logo-new.png
  humanURL: https://developers.google.com/drive/
  baseURL: https://www.googleapis.com//drive/v3//teamdrives/{teamDriveId}
  tags: Team Drive
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-drive/master/_listings/google-drive/teamdrivesteamdriveid-patch-openapi.md
- name: Google Drive
  x-api-slug: google-drive
  description: Google Drive is a file storage and synchronization service operated
    by Google. It allows users to store files in the cloud, synchronize files across
    devices, and share files. Google Drive encompasses Google Docs, Sheets and Slides,
    an office suite that permits collaborative editing of documents, spreadsheets,
    presentations, drawings, forms, and more.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-drive-logo-new.png
  humanURL: https://developers.google.com/drive/
  baseURL: https://www.googleapis.com//drive/v3
  tags: Google Drive
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-drive/master/_listings/google-drive/openapi.md
x-common:
- type: x-best-practices
  url: https://developers.google.com/drive/v3/web/practices
- type: x-branding-guidelines
  url: https://developers.google.com/drive/v3/web/marketing
- type: x-change-log
  url: https://developers.google.com/drive/release-notes
- type: x-code
  url: https://developers.google.com/drive/v3/web/downloads
- type: x-documentation
  url: https://developers.google.com/drive/v3/web/about-sdk
- type: x-github
  url: https://github.com/googledrive
- type: x-issues
  url: https://code.google.com/a/google.com/p/apps-api-issues/issues/list?q=API%3DDrive
- type: x-performance
  url: https://developers.google.com/drive/v3/web/performance
- type: x-support
  url: https://developers.google.com/drive/v3/web/support
- type: x-website
  url: https://developers.google.com/drive/
include: []
maintainers:
- FN: Kin Lane
  x-twitter: apievangelist
  email: info@apievangelist.com
---