# Authentication

> Don't forget to replace `abcd1234` with your Organization Key
> and `abcdefghij0123456789` with your Token!

```ruby
require 'net/http'
require 'json'

uri = URI.parse("https://api.scripted.com/abcd1234/v1/industries")
Net::HTTP.start(uri.host, uri.port, use_ssl: true) do |http|
  request = Net::HTTP::Get.new(uri)
  request["Content-Type"] = "application/json"
  request["Authorization"] = "Bearer abcdefghij0123456789"
  response = http.request request
  parsed = JSON.parse(response.body)
end
```

```shell
curl -H "Authorization: Bearer abcdefghij0123456789" \
    https://api.scripted.com/abcd1234/v1/industries
```

We use two factors to authenticate requests, an **Organization Key** and a **JSON Web Token**. You can find both of them in your Scripted dashboard by navigating to Account Settings and clicking on the API tab. All requests are namespaced under the relevant **Organization Key**, for example:

`GET /v1/abcd1234/jobs`

**Tokens** are passed as a `Bearer` in the `Authorization` header, like so:

`Bearer abcdefghij0123456789`

All requests must be made over `HTTPS`.
