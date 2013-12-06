**Contents**

 * [Content Server](#content-server)
  * [API Methods](#api-methods)
  * [Content Object](#content-object)
  * [Examples](#examples)
    * [Create content](#create-content)
    * [Upload source file](#upload-source-file)
    * [Upload alternate cover image](#upload-alternate-cover-image)
    * [Update content record](#upload-content-record)
  
## Content Server

A [RESTful API](http://en.wikipedia.org/wiki/Representational_state_transfer) exists for interacting with the CMS. By default the server lives at port 9000 on the localhost.

### API Methods

 * **/content**
  * POST: Create new Content record
    * Parameters: Content object
    * Response: Content object
 * **/content/:content_id**
  * GET: Retrieve Content record
    * Parameters: None
    * Response: Content object
  * PUT: Update Content record
    * Parameters: Key/value pairs of fields to be updated
    * Response: Content object
 * **/content/:content_id/source**
  * PUT: Upload content source file (currently only epub files are supported)
    * Parameters: Binary file data in request body
    * Response: CMS file_id for the uploaded file
  * GET: Download content source file
    * Parameters: None
    * Response: Binary file
 * **/content/:content_id/cover**
  * PUT: Upload alternate cover image for Content
    * Parameters: Image data in request body
    * Response: CMS file_id for the uploaded file
  * GET: Download alternate cover image
    * Parameters: None
    * Response: If file is found, server responds with binary file. If not found, server responds with 404 Not Found response header.

### Content Object

This section describes the structure of a Content object.

#### Common Parameters

All fields must be set when creating a new Content item, except fields marked as optional:

<dl>
<dt>user_id</dt>
<dd>Int. Content owner's numeric user ID from the Byblio WebApp database.</dd>
<dt>account_id</dt>
<dd>Int. Content owner's numeric account ID.</dd>
<dt>library_id</dt>
<dd>Int. Numeric ID of the library that contains this item.</dd>
<dt>type</dt>
<dd>String. Describes the kind of content stored in this record. Values accepted: 'publication', 'model', 'video', 'audio', 'photograph', 'social_media', 'slideshow'.
</dd>
<dt>title</dt>
<dd>
Object:
<dl>
<dt>value</dt>
<dd>String. Title text value</dd>
<dt>charset (optional)</dt>
<dd>String. ISO Character Set for title text</dd>
</dl>
</dd>
<dt>author</dt>
<dd>
Object:
<dl>
<dt>value</dt>
<dd>String. Author name</dd>
<dt>charset (optional)</dt>
<dd>String. ISO Character Set for author's name</dd>
</dl>
</dd>
<dt>description</dt>
<dd>
Object:
<dl>
<dt>value</dt>
<dd>String. Description text</dd>
<dt>charset</dt>
<dd>String. ISO Character Set for descripion text</dd>
</dl></dd>
<dt>publication_year</dt>
<dd>String. Date of publication.</dd>
<dt>publisher</dt>
<dd>String. Publisher's name.</dd>
<dt>publication_identifiers (optional)</dt>
<dd>Array. One or more objects describing the content's publication identifiers (i.e. ISBN):
<dl>
<dt>type</dt>
<dd>String. Identifier name (i.e. 'ISBN').</dd>
<dt>value</dt>
<dd>String. Identifier value (i.e. '0060572345')</dd>
</dl>
<dt>genre</dt>
<dd>String. One of the following: 'fiction', 'nonfiction'.</dd>
<dt>publication_reference (optional)</dt>
<dd>Array containing one or more strings for Harvard referencing.</dd>
</dl>

#### Internal Parameters

Content records from the CMS will also have the following fields defined. They are not to be altered and are for internal use only:

<dl>
<dt>date_created</dt>
<dd>Timestamp of when the Content record was created.</dd>
<dt>last_indexed</dt>
<dd>Timestamp for when the Content record was last indexed for search by Solr</dd>
<dt>cover_image_file_id</dt>
<dd>Internal CMS file_id of the Content item's alternate cover image</dd>
</dl>
</dl>

### Examples






## Web Server

tbd