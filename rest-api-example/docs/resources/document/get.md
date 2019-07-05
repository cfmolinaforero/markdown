[Back to Home](/rest-api-example/docs)

# Document Entity

## GET

There are three ways to retrieve document entities:

_Gets all the documents:_

```
GET http://site.com/api/documents
```

_Gets a document by id 4:_

```
GET http://site.com/api/documents/4
```

_Gets all the documents with the tag "code"_

```
GET http://site.com/api/documents?tag=code
```

### Request Data

All of the data for the `GET` requests are passed via the URL so there is no request body content expected.

### Response Data

**Multiple documents**

```javascript
[
  {
    id: "1",
    title: "Getting Started",
    body: "Learning to code...",
    tag: "code"
  },
  {
    id: "2",
    title: "Variables",
    body: "What are variables...",
    tag: "code"
  }
];
```

**Single document**

```javascript
{
    "id": "1",
    "title": "Getting Started",
    "body": "Learning to code...",
    "tag": "code"
}
```
