# Contribution Type

The [Contribution Type](#) describes the type of the contribution for a stakeholder.

## Schema

```json
{
  "@id": "iscn:contributionType",
  "@type": "rdf:Property",
  "rdfs:comment": "The type of the contribution. For interoperability, users are encouraged to use existing schema IRIs (e.g. http://schema.org/author, http://schema.org/publisher, http://schema.org/citation, http://schema.org/isBasedOn, http://schema.org/hasPart) for this field.",
  "rdfs:label": "contributionType",
  "schema:domainIncludes": [
    {
      "@id": "iscn:StakeholderInfo"
    }
  ]
}
```

## Sample
```json
"http://schema.org/author"
```


## Description

| Property | Occurs | Expected Type | Description |
| -------- | ------ | ------------- | ----------- |
|  |
