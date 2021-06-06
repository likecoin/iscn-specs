# Footprint

The [Footprint](#) describes contributions referring to other contents (e.g. citation or derivative works), this indicates the IRI (URI) of the referred content.

## Schema

```json
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
```

```json
"iscn://{registry_name}/{content_id}/{version}"
```


## Description

| Property    | Occurs | Expected Type | Description                                                                                                                   |
| ----------- | ------ | ------------- | ----------------------------------------------------------------------------------------------------------------------------- |
| context     | 1      | URL           | The location of this schema:<br>[https://iscn.io/schema/entity-v1](https://iscn.io/schema/entity-v1)                          |
| id          | 1      | String \| URI | The `id` property represents any kind of identifier for everything, and it should represent in either as String or URI links. |
| name        | 0~1    | String        | The `name` shows the display name of the entity.                                                                              |
| description | 0~1    | String        | The `description` shows a brief description of the entity.  
