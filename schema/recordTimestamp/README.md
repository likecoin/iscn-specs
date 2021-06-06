# Record Timestamp

The [TimePeriod](#) is timestamp of the current version of the ISCN record, recorded by the registry, in ISO 8601 format.

## Schema

```json
{
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

| Property | Occurs | Expected Type | Description |
| -------- | ------ | ------------- | ----------- |
