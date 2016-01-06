# Specialties

```ruby
ScriptedClient::Specialty.all
```

```shell
curl -H "Authorization: Bearer abcdefghij0123456789" \
    https://api.scripted.com/abcd1234/v1/specialties
```

> Sample Specialty

```json
{
  "id": "5654ebfc93be3b2c623b6eb1",
  "name": "Video Games"
}
```

`GET /:organization_key/v1/specialties`

If you're willing to pay a bit more (see [JobTemplate#pricing](#job-templates)) for a Specialist writer, you can include a Specialty (instead of a list of [Industries](#industries)) when you create a [Job](#jobs) or [Pitchset](#pitchsets).
