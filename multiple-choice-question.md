```YAML
---
title: Sample Question
type: select_one
shuffle_options: [false]
blooms: [3]
correct_response: b
options:
  - id: a
    text: "`fileset(id_rsa.pub)`"
  - id: b
    text: "`file(id_rsa.pub)`"
  - id: c
    text: "`filebase64(id_rsa.pud)`"
  - id: d
    text: "`templatefile(id_rsa.pub)`"
  - id: e
    text: "`filebase64(id_rsa.pub)`"
  - id: f
  - text: "None of the above"
  - id: g
  - text: "Any of the above"
---
```

A developer needs to write Terraform code that requires input from a local file named `id_rsa.pub`. Terraform has several built-in commands for reading files: `file`, `filebase64`, `fileexists`, and `templatefile`. Which built-in Terraform command should the developer use?
