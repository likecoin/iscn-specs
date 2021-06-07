# Record Notes

The [Record Notes](#) is a summary on the current record version, similar to Git commit logs.

## Schema

```json
{
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
