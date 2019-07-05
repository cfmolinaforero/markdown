# MdSlimDocs REST API

The REST API for MdSlimDocs provides CRUD support for working with resources used by the platform.

- [API Key](#api-key)
- [Resources](#resources)

## API Key

You will need to obtain an API key by logging into the admin of the isntance of MdSlimDocs and navigating to _Tools -> API Access_. Click on `Generate Key` to create a new key. You will need to include that key in all of your request headers to the API endpoints.

_Raw HTTP header_

```
GET http://site.com/api/documents
Accept: applicaiton/json
Authorization: Basic [YourKey]
```

Examples for setting the header value:

_JavaScript (AngularJS \$http)_

```javascript
$http.get("http://site.com/api/documents", {
  headers: {
    Authorization: "Basic " + yourToken
  }
});
```

_PHP_

```php
header('Accept', 'application/json');
header('Authorization', 'Basic ' .
$yourToken);
```

_C#_

```csharp
var webRequest = WebRequest.
    CreateHttp("http://site.com/api/documents");
webRequest.Method = "GET";
webRequest.Accept = "application/json";
webRequest.Headers["Authorization"] =
    string.Format("Basic {0}", yourToken);
```

## Resources

Details and examples for each REST verb can be found via the links under each resource type.

**Document**

- [GET](/rest-api-example/docs/resources/document/get.md)
- [POST](/rest-api-example/docs/resources/document/post.md)
- [PUT](/rest-api-example/docs/resources/document/put.md)
- [DELETE](/rest-api-example/docs/resources/document/delete.md)
