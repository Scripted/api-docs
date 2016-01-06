# Jobs

> Sample Job

```json
{
  "id": "5654ec06a6e02a37e7000318",
  "topic": "Where to buy an Orangutan",
  "state": "copyediting",
  "quantity": 1,
  "delivery": "standard",
  "deadline_at": "2015-12-04T01:30:00Z",
  "created_at": "2015-11-24T23:00:22Z",
  "pitch": null,
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
    "total": 9900
  },
  "writer": {
    "id": "5654ec01a6e02a37e700003b",
    "nickname": "Bob L.",
    "favorite": true
  },
  "document": {
    "id": "5654ec06a6e02a37e700031a",
    "type": "Document"
  },
  "prompts": [
    {
      "id": "5654ec06a6e02a37e700031e",
      "kind": "checkbox",
      "label": "Goal",
      "description": "Select one or many",
      "value": [
        "Informed analysis"
      ],
      "answer_required": false,
      "value_options": [
        "Informed analysis",
        "Thought leadership",
        "Repurpose existing writing",
        "Promote topic",
      ]
    }
  ],
  "guidelines": [
    {
      "id": "5654ebfc93be3b2c623b6e63",
      "name": "Anecdotal",
      "kind": "Tone"
    }
  ],
  "industries": [
    {
      "id": "5654ebfc93be3b2c623b6e2a",
      "name": "Education"
    }
  ],
  "attachments": [

  ]
}
```

Jobs are at the very center of the Scripted domain model. They represent a request for writing to be fulfilled by one of our freelancers. They are forged from a [JobTemplate](#job-templates), and include either a list of [Industries](#industries) or a single [Specialty](#specialties). Specialist jobs are completed by freelancers with more depth of knowledge, so they cost a bit more.

`state` can be any of the following:


State | Meaning
---------- | -------
hold  |  Paused by a Scripted employee for further clarification.
awaiting author  |  Submitted to Writers but not yet claimed.
writing  |  In the process of being written.
copyediting  |  Being screened for plagiarism or reviewed by an Editor.
ready for review  |  First draft is ready and awaiting your revision requests.
revising  |  Writer is incorporating your revision requests.
ready for acceptance  |  Final draft is ready. You can either accept or reject.
accepted  |  Accepted and charged.
canceled  |  Canceled and not charged.
rejected  |  Rejected and not charged.
