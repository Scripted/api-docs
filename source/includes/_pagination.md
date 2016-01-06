# Pagination

```ruby
jobs = ScriptedClient::Job.all
jobs.has_next?
# => true
page_two = jobs.next
```

```shell
curl -H "Authorization: Bearer abcdefghij0123456789" \
    https://api.scripted.com/abcd1234/v1/jobs \
    -d next_cursor='MTQwMDg4OTU0NDoy'
```
> Sample Cursor

```json
{
  "data": [{}, {}, {}, {}, {}, {}, {}, {}, {}, {}, {}, {}, {}, {}, {}],
  "paging": {
    "has_next": true,
    "next_cursor": "MTQwMDg4OTU0NDoy"
  }
}
```

We use cursor-based pagination. A single API request returns `15` records by default. If a list is longer than `15` objects, we'll return the first page and a `next_cursor` that you can pass on your next request to the list endpoint.
