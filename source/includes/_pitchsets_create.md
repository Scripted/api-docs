## Create a Pitchset

```ruby
require 'scripted_client'

# First, find a JobTemplate that you'd like to use:

templates = ScriptedClient::JobTemplate.all
blog_post = templates.find { |template| template.name == 'Standard Blog Post' }

# Next, assign some values for the Prompts on that JobTemplate.

key_points = blog_post.prompts.find { |prompt| prompt.label == 'Key Points' }
key_points.value = ['Orangutans make great pets', 'Normal pets are lame']

# Next, you can find an Industry:

industries = ScriptedClient::Industry.all
lifestyle = industries.find { |industry| industry.name == 'Lifestyle & Travel' }

# Now you can create the Pitchset!

pitchset = ScriptedClient::Pitchset.new(
  tagline: 'Cool Ideas for Zoo-centric Content',
  number_of_jobs_requested: 3,
  job_template: blog_post,
  industries: [lifestyle]
)
pitchset.save
# => true
```

```shell
curl -H "Authorization: Bearer abcdefghij0123456789" \
  https://api.scripted.com/abcd1234/v1/pitchsets \
    -d tagline="Cool Ideas for Zoo-centric Content" \
    -d number_of_jobs_requested=3 \
    -d job_template[id]=5ceb8bb8235bcc76bf475e21 \
    -d job_template[prompts][][id]=52cdda2f8b588f7e02000062 \
    -d job_template[prompts][][value]=Yes \
    -d job_template[prompts][][id]=52cdda2f8b588f7e02000064 \
    -d job_template[prompts][][value]=#apifuntimes \
    -d guidelines[][id]=e9d378cc8e74b4b5faa34892935d5665 \
    -d guidelines[][id]=689ca0246221f2f21e80e9dac9387bce \
    -d industries[][id]=8af7c7ae67b6d0854051378b9f3eede4 \
    -d industries[][id]=92e4132ea0560de3c12f072dc9a81486 \
    -d industries[][id]=f0709aabc7050b3eed7c43db83f0f4cf
```

`POST /:organization_key/v1/pitchsets`

Creating a Pitchset is very similar to creating a Job. Pass a [JobTemplate](#job-templates) and answers for that JobTemplate's [Prompts](#prompts). Either a list of [Industries](#industries) or a single [Specialty](#specialties) must also be included. Guidelines are optional.

<aside class="warning">The JobTemplate you pick must have a ContentFormat whose pitchable is true!</aside>

Parameter | Description
--------------------------------- | -------
`job_template`  |  **Required** Pick a `JobTemplate` with a `ContentFormat` whose `pitchable` is true.
`tagline` |  **Required** Attract and engage writers with a catchy tagline.
`number_of_jobs_requested`  |  **Optional** We'll pitch you twice as many ideas as the number of jobs you request.  Defaults to `1`.
`industries`  |  **Required unless Specialty is passed** A list of high-level categories pertaining to your job.
`specialty`  |  **Required unless Industries are passed** A deeper field of knowledge.
`guidelines`  |  **Optional** Tone, Voice and Perspective.
