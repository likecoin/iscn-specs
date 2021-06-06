# Stakeholders

The [Stakeholders](#) holds a list of [Stakeholder](../stakeholder/v1.md) and defines the ratio of profit sharing to each of the stakeholders.

## Schema

```json
{
  "@id": "iscn:stakeholders",
  "@type": "rdf:Property",
  "rdfs:comment": "Who or which content should be cited for the contribution to the content, and how much should the contribution be rewarded if someone wants to reward the content.",
  "rdfs:label": "stakeholders",
  "schema:domainIncludes": [
    {
      "@id": "iscn:Record"
    }
  ],
  "schema:rangeIncludes": [
    {
      "@id": "iscn:StakeholderInfo"
    }
  ]
}
```

## Sample

```json
[
  {
    "entity": {
      "@id": "http://github.com/nnkken",
      "name": "Chung Wu"
    },
    "rewardProportion": 95,
    "contributionType": "http://schema.org/author"
  },
  {
    "rewardProportion": 5,
    "contributionType": "http://schema.org/citation",
    "footprint": "https://en.wikipedia.org/wiki/Fibonacci_number",
    "description": "The blog post referred the matrix form of computing Fibonacci numbers."
  }
]
```

## Description

| Property     | Occurs | Expected Type                           | Description                                                                                                      |
| ------------ | ------ | --------------------------------------- | ---------------------------------------------------------------------------------------------------------------- |
| context      | 1      | URL                                     | The location of this schema:<br>[https://iscn.io/schema/stakeholders-v1](https://iscn.io/schema/stakeholders-v1) |
| stakeholders | 1      | \[[Stakeholder](../stakeholder/v1.md)\] | An array of [Stakeholder](../stakeholder/v1.md).                                                                 |
