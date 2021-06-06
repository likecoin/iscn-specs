# ISCN Record

The [ISCN](#) is the core metadata that acts as a kernel of ISCN, and it connects the content itself, the stakeholders and the intellectual property rights with a unique global identifier.

## Schema

```json
{
  "@id": "iscn:Record",
  "@type": "rdfs:Class",
  "rdfs:comment": "An ISCN record, recording the metadata of the content. The registry generating this record should create a unique identifier (the ISCN ID) for this record.",
  "rdfs:label": "Record",
  "rdfs:subClassOf": {
    "@id": "schema:Thing"
  }
}
```

                                                                                                                                                                                                            |

## Sample

```json
{
    "@context": {
        "@vocab": "http://iscn.io/",
        "recordParentIPLD": {
            "@container": "@index"
        },
        "stakeholders": {...},
        "contentMetadata": {...}
    },
    "@type": "Record",
    "@id": "iscn://likecoin-chain/btC7CJvMm4WLj9Tau9LAPTfGK7sfymTJW7ORcFdruCU/2",
    "recordTimestamp": "2021-03-23T12:00:00+08:00",
    "recordVersion": 2,
    "recordNotes": "Add IPFS fingerprint",
    "recordParentIPLD": {
        "/": "bahuaierav3bfvm4ytx7gvn4yqeu4piiocuvtvdpyyb5f6moxniwemae4tjyq"
    },
    "contentFingerprints": [
        "hash://sha256/9564b85669d5e96ac969dd0161b8475bbced9e5999c6ec598da718a3045d6f2e",
        "ipfs://QmNrgEMcUygbKzZeZgYFosdd27VE9KnWbyUD73bKZJ3bGi"
    ],
    "stakeholders": [...],
    "contentMetadata": {...
    }
}
```

## Description

| Property     | Occurs           | Expected Type                                | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| ------------ | ---------------- | -------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| context      | 1                | URL                                          | The location of this schema:<br>[https://iscn.io/schema/iscn-v1](https://iscn.io/schema/iscn-v1)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| id           | 1                | String                                       | This is the identifier of ISCN, and it is in the format:<br>`<registry-code>/<unique-id>[/<version>]`<br><br>`registry-code`: The reserved code for a [registry](../../README.md#iscn-content-registry).<br>`unique-id`: Any string contains alphanumeric and hyphens which is `[a-z][A-Z][0-9]-`, provided that is unique within the given [registry](../../README.md#iscn-content-registry).<br>`version`: Once the digital content is registered, the version counts as **1**. When there is any update later, the version number will go up one by one. Whenever the version is going up, the `registry-code` and `unique-id` must keep the same. Otherwise, it is an invalid ISCN. The version is optional, and if it does not provide, it means the latest version.<br><br>For example:<br>`1/abc-xyz-123`: Latest version of the ID `abc-xyz-123` and from registry 1<br>`2/music-010-1234/3`: Version 3 of the ID `music-010-1234` and from registry 2. |
| timestamp    | 1                | DateTime                                     | The timestamp of the creation or the modification of the ISCN record. It should be a human-readable DateTime and recommends to use ISO 8601.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| version      | 1                | Number                                       | Once the digital content is registered, the version counts as **1**. When there is any update later, the version number will go up one by one.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| parent       | 0<sup>\*</sup>~1 | [<u>ISCN</u>](#)                             | A [linked data](../../README.md#linked-data) to the previous version of the ISCN record which means the `registry-code` and `unique-id` in ISCN ID must be same. Otherwise, it counts as an invalid ISCN record.<br><br>_\* Only if the version is **1**, otherwise parent must be linked._                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| rights       | 1                | [<u>Rights</u>](../rights/v1.md)             | A [linked data](../../README.md#linked-data) to the intellectual property rights information.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| stakeholders | 1                | [<u>Stakeholders</u>](../stakeholders/v1.md) | A [linked data](../../README.md#linked-data) to an array of information of stakeholders.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| content      | 1                | [<u>Content</u>](../content/v1.md)           | A [linked data](../../README.md#linked-data) to the content metadata.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
