## Show a Pitchset

> Don't forget to replace `5ceb8bb8235bcc76bf475e21` with the `ID` of one of your pitchsets!

```ruby
ScriptedClient::Pitchset.find('5ceb8bb8235bcc76bf475e21')
```

```shell
curl -H "Authorization: Bearer abcdefghij0123456789" \
    https://api.scripted.com/abcd1234/v1/pitchsets/5ceb8bb8235bcc76bf475e21
```

`GET /:organization_key/v1/pitchsets/:id`
