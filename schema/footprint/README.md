# Footprint

The [Footprint](#) describes contributions referring to other contents (e.g. citation or derivative works), this indicates the IRI (URI) of the referred content.

## Schema

````json
{
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
```                                                                  |

## Sample

```json
"https://en.wikipedia.org/wiki/Fibonacci_number"
````

```json
"iscn://{registry_name}/{content_id}/{version}"
```

## Description

| Property | Expected Type | Description               |
| -------- | ------------- | ------------------------- |
| context  | String/URI    | URI of the reference work |
