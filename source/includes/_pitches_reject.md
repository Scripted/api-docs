## Reject a Pitch

```ruby
pitchset = ScriptedClient::Pitchset.requires_action.first
pitch = pitchset.pitches.first
pitch.reject("This is some optional feedback to the Writer")
```

```shell
curl -H "Authorization: Bearer abcdefghij0123456789" \
    https://api.scripted.com/abcd1234/v1/pitchsets/5ceb8bb8235bcc76bf475e21/pitches/5def8bb8235bcc76bf345d5e/reject \
    -d feedback="Not quite what we were looking for. Try making it funnier."
```

`POST /:organization_key/v1/pitchsets/:pitchset_id/pitches/:id/reject`

You can pass `feedback` in the body of the `POST` request to `reject` a Pitch. Feedback will be passed along to the writer for guidance in coming up with future topic ideas.
