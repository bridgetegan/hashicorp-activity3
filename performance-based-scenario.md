---
title: "Sample Scenario"
---
### Your Environment

There is a single HashiCorp Vault cluster:

 `scenario-cluster-vault`
 
* Vault Address: `127.0.0.1:8200`
* Vault Token: `s.f7Ea3C3ojOYE0GRLzmhSG`

The AppRole auth method has been enabled on the `approle/` path. A role has been created and has the following properties:
* Role Name: `appy7`
* Vault policy: `policy7`
* Roll ID: xxxxxxxx-xxxxxxxx-xxxxxxxx-xxxxxxxxxxx

Additionally, there is an application server:
`scenario-node-appserver`
 
* Server Address: <IP_Address>
* Vault agent Config File: `/etc/vault/agent7.hcl`
* Sink Location: `/etc/vault/token.json`
* The Vault binary is already in the `$PATH`

### Instructions
You have an application that needs to retrieve credentials from Vault, but it is not currently architected to interact directly with Vault. You need to securely configure Vault Agent Auto-Auth and token sink, so the Vault Agent will retrieve a Vault token and keep it automatically renewed.

1. Using the information provided above, configure the application server to use the Vault Agent to retrieve a Vault Token. 
* The Vault Agent should use approle for authentication, so a SecretID needs to be generated in Vault. 
* The resulting token from Vault should be protected using response wrapping on the auth method. 
* Write the token to the `token.json` file path.

### Important Notes
You can validate the configuration by viewing the contents of the sink. If a token does not exist, the configuration is not correct.

