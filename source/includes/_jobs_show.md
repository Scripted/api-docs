## Show a Job

> Don't forget to replace `5ceb8bb8235bcc76bf475e21` with the `ID` of one of your jobs!

```ruby
ScriptedClient::Job.find('5ceb8bb8235bcc76bf475e21')
```

```shell
curl -H "Authorization: Bearer abcdefghij0123456789" \
    https://api.scripted.com/abcd1234/v1/jobs/5ceb8bb8235bcc76bf475e21
```

## Get a Job's HTML Contents

```ruby
ScriptedClient::Job.find('5ceb8bb8235bcc76bf475e21').html_contents
```

```shell
curl -H "Authorization: Bearer abcdefghij0123456789" \
    https://api.scripted.com/abcd1234/v1/jobs/5ceb8bb8235bcc76bf475e21/html_contents
```
To retrieve the actual writing, you have to hit a separate endpoint. It returns an Array of HTML Strings.
