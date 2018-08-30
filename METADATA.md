# Metedata Guidelines



## Company Rules

- A user must consent to uploading their data with Metadata.
- Metadata associated with any record will be permanent, searchable and public and therefore there needs to be consent.
- It is best that unconsented Metadata is not appended to Linnia Smart Contracts. 
- This functionality should be at App Level and if a user does not consent then data uploaded to Linnia Protocol should be void of Metadata. 
- Please take caution, show examples of Metadata and be completely transparent in how a user's data and Metadata are uploaded to the application. It is in the best interest of everyone involved that the privacy of the user is maintained at all times. 



# Specifications

The Linnia protocol stores Metadata for every record that is added to the protocol. This Metadata is public and is used to query the data and understand what is stored in every record without really having access to the data inside.



## Example

```json
{
    "data_format": "json",
    "domain": "social media",
    "storage": "IPFS",
    "encryption_scheme": "x25519-xsalsa20-poly1305",
    "encryption_public_key": "hQYhHJpzZH/tGhz1wtqSjkL17tJSnEEC4yVGyNTHNQY=",
    "linnia_js_version": "0.1.4",
    "owner_name": "John Linnia",
    "provider_name": "Facebook",
    "provider_ethereum_address": "0x349e31e92027f86b0ffeb5cd5e07003c7f229872",
    "keywords": [ "facebook", "friends list", "people" ],
}
```



## Specifications

The Metadata should be in JSON format and the following are the properties that should have:

| property                  | type          | options                     | required |                                                              |
| ------------------------- | ------------- | --------------------------- | -------- | ------------------------------------------------------------ |
| data_format               | string        | 'json'   'csv' 'plain_text' | Yes      | Format of the data                                           |
| domain                    | string        |                             | Yes      | Domain of the content                                        |
| storage                   | string        |                             | Yes      | Storage                                                      |
| encryption_scheme         | string        |                             | Yes      | Encryption Scheme used to encrypt the data                   |
| encryption_public_key     | string        |                             | Yes      | Encryption Public Key used to encrypt the data               |
| linnia_js_version         | string        |                             | Yes      | If the data was uploaded using Linnia js, this field will contain the version of the library used for compatibility reasons |
| owner_name                | string        |                             | No       | The name or identity of the owner                            |
| provider_name             | string        |                             | No       | The name or identity of the data provider if it was not uploaded by the same owner |
| provider_ethereum_address | address       |                             | Yes      | The Ethereum Address of the provider if it was not uploaded by the same owner |
| keywords                  | array<string> |                             | Yes      | An array of keywords in order to be able to search           |
