# Record Parent IPLD

The [Record Parent IPLD](#) is the IPLD hash of the previous version of this record, if any. For interoperability, it should fulfill the DAG-JSON IPLD codec, i.e. be an object containing a `/` key associated with a string value, which is the Base32 encoding of the CID of the parent record.

## Schema

```json
{
  "@context": {
    "rdf": "http://www.w3.org/1999/02/22-rdf-syntax-ns#",
    "rdfs": "http://www.w3.org/2000/01/rdf-schema#",
    "schema": "https://schema.org/",
    "iscn": "http://iscn.io/"
  },
  "@id": "iscn:recordParentIPLD",
  "@type": "rdf:Property",
  "rdfs:comment": "The IPLD hash of the previous version of this record, if any. For interoperability, it should fulfill the DAG-JSON IPLD codec, i.e. be an object containing a `/` key associated with a string value, which is the Base32 encoding of the CID of the parent record.",
  "rdfs:label": "recordParentIPLD",
  "schema:domainIncludes": [
    {
      "@id": "iscn:Record"
    }
  ]
}
```

## Sample

```json
{
  "/": "bahuaierav3bfvm4ytx7gvn4yqeu4piiocuvtvdpyyb5f6moxniwemae4tjyq"
}
```

## Description

| Property | Expected Type | Description                 |
| -------- | ------------- | --------------------------- |
| /        | String        | IPLD of parent ISCN record. |
