# Industries

```ruby
ScriptedClient::Industry.all
```

```shell
curl -H "Authorization: Bearer abcdefghij0123456789" \
    https://api.scripted.com/abcd1234/v1/industries
```

> Sample Industry

```json
{
  "id": "5654ebfc93be3b2c623b6e2f",
  "name": "Publishing & Journalism",
  "specialties": [
    {
      "id": "5654ebfc93be3b2c623b6eab",
      "name": "Self Publishing"
    }
  ]
}
```

`GET /:organization_key/v1/industries`

Industries specify the topic area of your [Job](#jobs) or [Pitchset](#pitchsets). They also have a list of associated [Specialties](#specialties) if you'd like a Writer with more depth of knowledge.
