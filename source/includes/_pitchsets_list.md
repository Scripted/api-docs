## List all Pitchsets

```ruby
ScriptedClient::Pitchset.all

# Or if you want to filter by state

ScriptedClient::Pitchset.requires_action
```

```shell
curl -H "Authorization: Bearer abcdefghij0123456789" \
    https://api.scripted.com/abcd1234/v1/pitchsets

# Or if you want to filter by state

curl -H "Authorization: Bearer abcdefghij0123456789" \
    https://api.scripted.com/abcd1234/v1/pitchsets/requires_action
```

`GET /:organization_key/v1/pitchsets`

You can pass any of the following filters to narrow your search:

Filter | Meaning
---------- | -------
open  |  All Pitchsets in `active`, `full`, and `idle` states. The "Active" section of your "Topic Pitches" tab in the Scripted dashboard.
closed  |  All Pitchsets in `marked_complete` and `auto_closed` states. The "Archived" section of your "Topic Pitches" tab in the Scripted dashboard.
requires_action  |  Pitchsets in the `open` state with at least one pending Pitch. The "Action Items" tab in the Scripted dashboard.

