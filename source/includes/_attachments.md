# Attachments

Files to assist Scripted.com writers.

## Example object

    {
      "id": "3b9bc709aba13134e3c50aa4",
      "name": "chuck-testa",
      "kind": "Data",
      "description": "Attachments with descriptions are best",
      "url":  "https://cdn.example.com/s/ibqzw2tbwdmtzlpkjjpo"
      "created_at": "2014-10-01T10:58:01-07:00",
      "job": {
       "id": "e7a21af4d5c668a1d36d1401"
      }
    }

## Create an Attachment

`POST https://api.scripted.com/abcd1234/v1/attachments`

#### Parameters

* `file` *file*

#### Example request

    curl \
      -H "Authorization: Token token=abcdefghij0123456789" \
      -include --form file=@/Users/Duder/Desktop/clues.pdf \
      https://api.scripted.com/abcd1234/v1/jobs/e7a21af4d5c668a1d36d1401/attachments \
      -v

#### Example response

    {
      "data": {
        "id": "545d6ef3be15d6062a000001",
        "name": "in-n-out.gif",
        "description": null,
        "kind": "Data",
        "url": "https://cdn.example.com/image.gif",
        "created_at": "2014-11-07T17:16:36-08:00",
        "job": {
          "id": "54594b77eba2ddf697000001"
        }
      }
    }

## <a name="pagination"></a>Pagination

The Scripted.com API offers cursor-based pagination. A single API request
returns `30` records by default.

### <a name="cursors"></a>Cursors

If lists are long, the API returns partial results and you will see the
following JSON response:

    {
      "data": [...],
      "paging": {
        "has_next": true
        "next_cursor": 'MTQwMDg4OTU0NDoy'
        }
      }
    }

### <a name="paging-parameters"></a>Paging parameters

<table>
  <thead>
    <tr>
      <th>Name</th>
      <th>Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><em>has_next</em></td>
      <td>Boolean value indicating whether additional pages exist</td>
    </tr>
    <tr>
      <td><em>next_cursor</em></td>
      <td>Random string of characters marking a specific item in the list</td>
    </tr>
  </tbody>
</table>

When `has_next` contains the value `true` clients may supply the `next_cursor`
parameter to request the next page of results

#### Example request

    curl -H "Authorization: Token token=abcdefghij0123456789" \
    https://api.scripted.com/abcd1234/v1/jobs \
    -d next_cursor='MTQwMDg4OTU0NDoy'

#### Example response

    {
      "data": [...],
      "paging": {
        "has_next": false,
        "next_cursor": 'MTQwMDg4OTU0NDoz'
        }
      }
    }
