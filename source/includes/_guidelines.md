# Guidelines

```ruby
ScriptedClient::Guideline.all
```

```shell
curl -H "Authorization: Bearer abcdefghij0123456789" \
    https://api.scripted.com/abcd1234/v1/guidelines
```

> Sample Guideline

```json
{
  "id": "5654ebfc93be3b2c623b6e63",
  "name": "Anecdotal",
  "kind": "Tone"
}
```

`GET /:organization_key/v1/guidelines`

Guidelines are optional. [Jobs](#jobs) and [Pitchsets](#pitchsets) can have many of them.
