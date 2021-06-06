# Entity

The [Entity](#) describes the necessary information of an entity, and all specific entity should inherit from [Entity](#) to extend.

## Schema

```json
{
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

| Property    | Occurs | Expected Type | Description                                                                                                                   |
| ----------- | ------ | ------------- | ----------------------------------------------------------------------------------------------------------------------------- |
| context     | 1      | URL           | The location of this schema:<br>[https://iscn.io/schema/entity-v1](https://iscn.io/schema/entity-v1)                          |
| id          | 1      | String \| URI | The `id` property represents any kind of identifier for everything, and it should represent in either as String or URI links. |
| name        | 0~1    | String        | The `name` shows the display name of the entity.                                                                              |
| description | 0~1    | String        | The `description` shows a brief description of the entity.                                                                    |
