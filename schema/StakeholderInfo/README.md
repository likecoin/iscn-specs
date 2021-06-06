# Stakeholder


The [Stakeholder](#) is the information about the stakeholder, including the [Entity](../entity/v1.md) of the stakeholder and profit sharing ratio hint. Also, if the current digital work is a derivative work, then the source of underlying work is also registered as a creation footprint.

## Schema

```json
{
  "@id": "iscn:StakeholderInfo",
  "@type": "rdfs:Class",
  "rdfs:comment": "One entry of the stakeholder list of the content, describing who or which content should be cited for the contribution to the content, and how much should the contribution be rewarded.",
  "rdfs:label": "StakeholderInfo",
  "rdfs:subClassOf": {
    "@id": "schema:Thing"
  }
}
```

## Sample

```json
{
    "entity": {
        "@id": "http://github.com/nnkken",
        "name": "Chung Wu"
    },
    "rewardProportion": 95,
    "contributionType": "http://schema.org/author"
}
```

## Description

Property|Occurs|Expected Type|Description
--|--|--|--
