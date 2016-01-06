# Prompts

> Sample Prompt

```json
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
}
```

Prompts are question/answer pairs that help guide your writer. They can be one of five kinds: `string[255]` `string[1024]` `radio` `checkbox` `array`. The data type of the `value` that you post will depend on the kind of the Prompt:

| Kind         | Value Type                    | Has `value_options`? |
|--------------|-------------------------------|----------------------|
| string[255]  | String (max. 255 characters)  | No                   |
| string[1024] | String (max. 1024 characters) | No                   |
| radio        | String                        | Yes                  |
| checkbox     | Array                         | Yes                  |
| array        | Array                         | No                   |

<aside class="warning">If a Prompt has value_options, the value you pass must be one of the options. If answer_required is true, you must provide a value.</aside>
