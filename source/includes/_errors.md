# Errors

> Errors are returned in an Array like so:

```json

    {
      "errors": [
        "Topic is too long (maximum is 255 characters)",
        "Quantity must be one of the ContentFormat's quantity_options"
      ]
    }

```

The Scripted API does not always return a `200 OK` status.

Status | Meaning
---------- | -------
400 | Bad Request -- The request was malformed in some way.
401 | Unauthorized -- The Token provided was invalid or expired.
403 | Forbidden -- The Token provided does not have access to the namespace's Organization Key.
404 | Not Found -- The specified resource could not be found
500 | Internal Server Error -- We had a problem with our server. Try again later.
503 | Service Unavailable -- We're temporarially offline for maintanance. Please try again later.
