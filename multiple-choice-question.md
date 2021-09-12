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

Terraform has several built-in commands for reading files: `file`, `filebase64`, `fileexists`, and `templatefile`. A developer needs to read some input from a local file called `id_rsa.pub` that resides in the same directory as the configuration used to import the file’s contents as a string. Which built-in Terraform command should the developer use based on this input?
