# Metadata Specifications

The Linnia protocol stores Metadata for every record that is added to the protocol. This Metadata is public and is used to query the data and understand what is stored in every record without really having access to the data inside.



## Example

```json
{
    "data_format": "json",
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



#### Data Format (data_format)

Format of the data, it has to be one of the following:

- json
- csv
- plain_text



#### Encryption Scheme (encryption_scheme)

Encryption Scheme used to encrypt the data



#### Encryption Public Key (encryption_public_key)

Encryption Public Key used to encrypt the data



#### Linnia js Version (linnia_js_version)

If the data was uploaded using Linnia js, this field will contain the version of the library used for compatibility reasons



#### [*optional] Owner Name (owner_name)

The name or identity of the owner. This field is completly optional



#### Provider Name (provider_name)

The name or identity of the data provider if it was not uploaded by the same owner



#### Provider Ethereum Address (provider_ethereum_address)

The Ethereum Address of the provider if it was not uploaded by the same owner



#### Keywords (keywords)

An array of as much keywords as you want in order to be able to search

