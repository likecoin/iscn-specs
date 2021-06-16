# Stakeholder

The [Stakeholder](#) is the information about the stakeholder, including the [Entity](../entity/README.md) of the stakeholder and profit sharing ratio hint. Also, if the current digital work is a derivative work, then the source of underlying work is also registered as a creation footprint.

## Schema

```json
{
  "@context": {
    "rdf": "http://www.w3.org/1999/02/22-rdf-syntax-ns#",
    "rdfs": "http://www.w3.org/2000/01/rdf-schema#",
    "schema": "https://schema.org/",
    "iscn": "http://iscn.io/"
  },
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

| Property         | Expected Type                                         | Description                                                  |
| ---------------- | ----------------------------------------------------- | ------------------------------------------------------------ |
| entity           | \[[entity](../entity/README.md)\]                     | An [entity](../entity/README.md) object.                     |
| rewardProportion | \[[rewardProportion](../rewardProportion/README.md)\] | An [rewardProportion](../rewardProportion/README.md) object. |
| contributionType | \[[contributionType](../contributionType/README.md)\] | An [contributionType](../contributionType/README.md) object. |
