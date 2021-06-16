# Entity

The [Entity](#) describes the necessary information of an entity, and all specific entity should inherit from [Entity](#) to extend.

## Schema

```json
{
  "@context": {
    "rdf": "http://www.w3.org/1999/02/22-rdf-syntax-ns#",
    "rdfs": "http://www.w3.org/2000/01/rdf-schema#",
    "schema": "https://schema.org/",
    "iscn": "http://iscn.io/"
  },
  "@id": "iscn:entity",
  "@type": "rdf:Property",
  "rdfs:comment": "Entity who should be cited and / or rewarded for the contribution on the content.",
  "rdfs:label": "entity",
  "schema:domainIncludes": [
    {
      "@id": "iscn:StakeholderInfo"
    }
  ],
  "schema:rangeIncludes": [
    {
      "@id": "schema:Thing"
    }
  ]
}
```

## Sample

```json
{
  "@id": "http://github.com/nnkken",
  "name": "Chung Wu"
}
```

## Description

| Property    | Expected Type | Description                                                                                                                   |
| ----------- | ------------- | ----------------------------------------------------------------------------------------------------------------------------- |
| id          | String \| URI | The `id` property represents any kind of identifier for everything, and it should represent in either as String or URI links. |
| name        | String        | The `name` shows the display name of the entity.                                                                              |
| description | String        | The `description` shows a brief description of the entity.                                                                    |
