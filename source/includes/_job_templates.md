# Job Templates

```ruby
ScriptedClient::JobTemplate.all
```

```shell
curl -H "Authorization: Bearer abcdefghij0123456789" \
    https://api.scripted.com/abcd1234/v1/job_templates
```

> Sample JobTemplate

```json
{
  "id": "5654ec02a6e02a37e70000cc",
  "name": "Standard Blog Post",
  "created_at": "2015-11-24T15:00:18-08:00",
  "content_format": {
    "id": "5654ec02a6e02a37e70000d5",
    "name": "Standard Blog Post",
    "pitchable": true,
    "length_metric": "350-450 words",
    "quantity_options": [
      1
    ]
  },
  "pricing": {
    "base": 9900,
    "specialist": 14900
  },
  "prompts": [
    {
      "id": "5654ec02a6e02a37e70000d8",
      "kind": "checkbox",
      "label": "Goal",
      "description": "Select one or many",
      "answer_required": false,
      "value_options": [
        "Informed analysis",
        "Thought leadership",
        "Repurpose existing writing",
        "Promote topic",
      ]
    },
    {
      "id": "5654ec02a6e02a37e70000da",
      "kind": "string[255]",
      "label": "Sample Blog",
      "description": "Link to an existing blog and describe why it's a good sample",
      "answer_required": false
    },
    {
      "id": "5654ec02a6e02a37e70000dc",
      "kind": "checkbox",
      "label": "Blog Structure",
      "description": "Select one or many",
      "answer_required": false,
      "value_options": [
        "Paragraphs",
        "Subheads",
        "Lists"
      ]
    },
    {
      "id": "5654ec02a6e02a37e70000de",
      "kind": "array",
      "label": "Key Points",
      "description": "List key points your writer should address",
      "answer_required": false
    },
    {
      "id": "5654ec02a6e02a37e70000e3",
      "kind": "radio",
      "label": "Links to Sources",
      "description": "Select one",
      "answer_required": false,
      "value_options": [
        "Include sources as linked anchor text",
        "Include sources as source list",
        "No sources"
      ]
    }
  ]
},
```

A JobTemplate has a [ContentFormat](#content-formats), such as a **Short Blog Post**, and a collection of [Prompts](#prompts) to that are designed to help guide your writer.
