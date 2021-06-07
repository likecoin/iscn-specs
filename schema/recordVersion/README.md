# Record Version

The [Record Version](#) is the version of the ISCN record. It could be different from the content's version, as one may update only the content metadata or ISCN record fields without modifying the content itself

## Schema

```json
{
  "@id": "iscn:recordVersion",
  "@type": "rdf:Property",
  "rdfs:comment": "The version of the ISCN record. It could be different from the content's version, as one may update only the content metadata or ISCN record fields without modifying the content itself.",
  "rdfs:label": "recordVersion",
  "schema:domainIncludes": [
    {
      "@id": "iscn:Record"
    }
  ],
  "schema:rangeIncludes": [
    {
      "@id": "schema:Number"
    }
  ]
}
```

## Sample

```json
2
```

## Description

| Property | Expected Type | Description                                                                                               |
| -------- | ------------- | --------------------------------------------------------------------------------------------------------- |
| -        | Number        | The version counts starts with 1. When there is any update later, the version number will go up one by 1. |
