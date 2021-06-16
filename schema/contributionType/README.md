# Contribution Type

The [Contribution Type](#) describes the type of the contribution for a stakeholder.

## Schema

```json
{
  "@context": {
    "rdf": "http://www.w3.org/1999/02/22-rdf-syntax-ns#",
    "rdfs": "http://www.w3.org/2000/01/rdf-schema#",
    "schema": "https://schema.org/",
    "iscn": "http://iscn.io/"
  },
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

| Property | Expected Type | Description                                                                                                 |
| -------- | ------------- | ----------------------------------------------------------------------------------------------------------- |
| -        | String        | The type of digital content, e.g [Author](http://schema.org/author), [Citation](http://schema.org/citation) |
