# Stakeholders

The [Stakeholders](#) holds a list of [Stakeholder](../stakeholder/README.md) and defines the ratio of profit sharing to each of the stakeholders.

## Schema

```json
{
  "@context": {
    "rdf": "http://www.w3.org/1999/02/22-rdf-syntax-ns#",
    "rdfs": "http://www.w3.org/2000/01/rdf-schema#",
    "schema": "https://schema.org/",
    "iscn": "http://iscn.io/"
  },
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

| Property     | Expected Type                                       | Description                                                  |
| ------------ | --------------------------------------------------- | ------------------------------------------------------------ |
| stakeholders | [StakeholderInfo](../StakeholderInfo/README.md)[] | An array of [StakeholderInfo](../StakeholderInfo/README.md). |
