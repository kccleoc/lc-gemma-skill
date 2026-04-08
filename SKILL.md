---
name: hello-world-js
description: Return a hello world message using a JS skill.
---

# Hello World JS Skill

## Instructions

You MUST use the `run_js` tool with the following exact parameters:
- script name: index.html
- data: A JSON string with the following fields:
  - name: The name to greet. String.

If the user does not provide a name, use:
```json
{"name":"world"}
```

Example:
```json
{"name":"Neo"}
```

After receiving the tool result, answer naturally using the returned text.
