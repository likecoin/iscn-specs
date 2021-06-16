# Footprint

The [Footprint](#) describes contributions referring to other contents (e.g. citation or derivative works), this indicates the IRI (URI) of the referred content.

## Schema

```json
{
  "@context": {
    "rdf": "http://www.w3.org/1999/02/22-rdf-syntax-ns#",
    "rdfs": "http://www.w3.org/2000/01/rdf-schema#",
    "schema": "https://schema.org/",
    "iscn": "http://iscn.io/"
  },
  "@id": "iscn:footprint",
  "@type": "rdf:Property",
  "rdfs:comment": "For contributions referring to other contents (e.g. citation or derivative works), this indicates the IRI (URI) of the referred content.",
  "rdfs:label": "footprint",
  "schema:domainIncludes": [
    {
      "@id": "iscn:StakeholderInfo"
    }
  ]
}
```

## Sample

```json
"https://en.wikipedia.org/wiki/Fibonacci_number"
```

```json
"iscn://{registry_name}/{content_id}/{version}"
```

## Description

| Property | Expected Type | Description               |
| -------- | ------------- | ------------------------- |
| -        | String/URI    | URI of the reference work |
