# Pitchsets

> Sample Pitchset

```json
{
  "id": "5654ec23a6e02a37e70006f2",
  "tagline": "Cool Ideas for Zoo-centric Content",
  "status": "active",
  "number_of_jobs_requested": 2,
  "number_of_pitches_accepted": 0,
  "number_of_pitches_rejected": 1,
  "number_of_pitches_awaiting_review": 0,
  "specialty": {
    "id": "5654ebfc93be3b2c623b6ea8",
    "name": "Physical Fitness"
  },
  "guidelines": [
    {
      "id": "5654ebfc93be3b2c623b6e60",
      "name": "1st Personal Singular",
      "kind": "Voice"
    }
  ],
  "industries": [],
  "attachments": [
    {
      "id": "568da92bfdcedc00e4000000",
      "name": "analytics.pptx",
      "description": "Use this data in your pitches",
      "kind": "Data",
      "url": "https://zoos.com/analytics.pptx",
      "created_at": "2016-01-06T15:54:19-08:00"
    }
  ],
  "prompts": [
    {
      "id": "5654ec23a6e02a37e70006f6",
      "kind": "string[255]",
      "label": "Target Audience",
      "description": "Describe the particular group at which your content is aimed",
      "value": "Kittens of all types: Frat Kittens, Gamer Kittens, Hackysack Kittens, Tech Kittens, and Kitten Kittens",
      "answer_required": false
    }
  ],
  "content_format": {
    "id": "5654ec02a6e02a37e70000d5",
    "name": "Standard Blog Post",
    "pitchable": true,
    "length_metric": "350-450 words",
    "quantity_options": [
      1
    ]
  }
}
```

Our writers can pitch you content ideas. A Pitchset is a lot like a [Job](#jobs) (it's forged from a [JobTemplate](#job-templates) with [Prompt](#prompts) answers, [Industries](#industries) and [Guidelines](#guidelines)), but instead of being a request for writing, it is a request for [topics to be pitched by our writers](#pitches).

`status` can be any of the following:

Status | Meaning
---------- | -------
active  |  Writers are generating topic pitches.
full  |  Writers have finished pitching ideas.
marked_complete  |  You archived the pitchset.
auto_closed  |  You accepted as many pitches as you initially requested.
idle  |  Writers are no longer pitching topics, because you have not responded to pitches.
