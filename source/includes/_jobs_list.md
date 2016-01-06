## List all Jobs

```ruby
ScriptedClient::Job.all

# Or if you want to filter by state

ScriptedClient::Job.draft_ready
```

```shell
curl -H "Authorization: Bearer abcdefghij0123456789" \
    https://api.scripted.com/abcd1234/v1/jobs

curl -H "Authorization: Bearer abcdefghij0123456789" \
    https://api.scripted.com/abcd1234/v1/jobs?filter=draft_ready
```

You can pass any of the following filters to narrow your results:

`screening` `writing` `draft_ready` `revising` `final_ready` `in_progress` `needs_review` `accepted` `rejected` `finished`

See [Pagination](#pagination) if you have more than 15 jobs.
