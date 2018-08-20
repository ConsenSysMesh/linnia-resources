# Metedata Guidelines

## Company Rules

  - A user must consent to uploading their data with Metadata.
  - Metadata associated with something uploaded to IPFS will be permanent, searchable and public and therefore there needs to be consent.
  - It is best that unconsented Metadata is not appended to Linnia Smart Contracts. 
  - This functionality should be at App Level and if a user does not consent then data uploaded to Linnia Protocol should be void of Metadata. 
  - Please take caution, show examples of Metadata and be completely transparent in how a user's data and Metadata are uploaded to the application. It is in the best interest of everyone involved that the privacy of the user is maintained at all times. 

## Metadata Standards

  - Metadata will be specific to domain (i.e Health, Social etc) 
  - Specific Metadata standards are currently being worked on and investigated. 
  
## Metadata and Personally Indentifiable Information (PII)

- The issuance of PII on the Ethereum Blockchain will most definitly be an issue for most people and will be up to the company, developer or application to properly disclose how Metadata for files are being uploaded. Customers will want to make sure their data is secure and that information that they do not want public is not out in the open. 
- When a person's name is included in the Metadata, someone can ultimately find out the person's Ethereum address through researching the blockchain. This should be kept in mind when uploading Metadata alongside data to Linnia. 

## Example

```
PII (Something a customer may not want to uplaoded alongside their data)
{
"Name":"Arron Trantow",
"Test": Glucose,
"Results: "190 mg/dL"
}
```
```
Non-PII (A solution that may work)
{
"Customer Number":"7494839843",
"Test": Glucose,
"Results: "190 mg/dL"
}
```

```
Non-PII (A solution stripped of all customer information)
{
"Test": Glucose,
"Results: "190 mg/dL"
}
```


