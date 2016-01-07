## List all Pitches within a Pitchset

```ruby
pitchset = ScriptedClient::Pitchset.all.first
pitchset.pitches
```

```shell
curl -H "Authorization: Bearer abcdefghij0123456789" \
    https://api.scripted.com/abcd1234/v1/pitchsets/5ceb8bb8235bcc76bf475e21/pitches
```

`GET /:organization_key/v1/pitchsets/:pitchset_id/pitches`
