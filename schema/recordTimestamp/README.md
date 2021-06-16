# Record Timestamp

The [TimePeriod](#) is timestamp of the current version of the ISCN record, recorded by the registry, in ISO 8601 format.

## Schema

```json
{
  "@context": {
    "rdf": "http://www.w3.org/1999/02/22-rdf-syntax-ns#",
    "rdfs": "http://www.w3.org/2000/01/rdf-schema#",
    "schema": "https://schema.org/",
    "iscn": "http://iscn.io/"
  },
  "@id": "iscn:recordTimestamp",
  "@type": "edf:Property",
  "rdfs:comment": "The timestamp of the current version of the ISCN record, recorded by the registry, in ISO 8601 format.",
  "rdfs:label": "recordTimestamp",
  "schema:domainIncludes": [
    {
      "@id": "iscn:Record"
    }
  ],
  "schema:rangeIncludes": [
    {
      "@id": "schema:DateTime"
    }
  ]
}
```

## Sample

```json
"2021-03-23T12:00:00+08:00"
```

## Description

| Property | Expected Type | Description                                                                                                                                  |
| -------- | ------------- | -------------------------------------------------------------------------------------------------------------------------------------------- |
| -        | String        | The timestamp of the creation or the modification of the ISCN record. It should be a human-readable DateTime and recommends to use ISO 8601. |
