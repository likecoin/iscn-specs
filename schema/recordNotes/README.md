# Record Notes

The [Record Notes](#) is a summary on the current record version, similar to Git commit logs.

## Schema

```json
{
  "@context": {
    "rdf": "http://www.w3.org/1999/02/22-rdf-syntax-ns#",
    "rdfs": "http://www.w3.org/2000/01/rdf-schema#",
    "schema": "https://schema.org/",
    "iscn": "http://iscn.io/"
  },
  "@id": "iscn:recordNotes",
  "@type": "rdf:Property",
  "rdfs:comment": "A summary on the current record version, similar to Git commit logs.",
  "rdfs:label": "recordNotes",
  "schema:domainIncludes": [
    {
      "@id": "iscn:Record"
    }
  ],
  "schema:rangeIncludes": [
    {
      "@id": "schema:Text"
    }
  ]
}
```

## Sample

```json
"Add IPFS fingerprint"
```

## Description

| Property | Expected Type | Description                  |
| -------- | ------------- | ---------------------------- |
| -        | String        | The note for the ISCN record |
