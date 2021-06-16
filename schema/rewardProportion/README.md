# Reward Proportion

The [Reward Proportion](#) is how much should the entity or footprinted content in this entry share a reward by proportion. Note that this is not forced, but simply a subjective guideline field from the uploader of this record. The value should always be greater than 0. For interoperability, integers are preferred over decimal numbers

## Schema

```json
{
  "@context": {
    "rdf": "http://www.w3.org/1999/02/22-rdf-syntax-ns#",
    "rdfs": "http://www.w3.org/2000/01/rdf-schema#",
    "schema": "https://schema.org/",
    "iscn": "http://iscn.io/"
  },
  "@id": "iscn:rewardProportion",
  "@type": "rdf:Property",
  "rdfs:comment": "If the content is rewarded, how much should the entity or footprinted content in this entry share the reward by proportion. Note that this is not forced, but simply a subjective guideline field from the uploader of this record. The value should always be greater than 0. For interoperability, integers are preferred over decimal numbers.",
  "rdfs:label": "rewardProportion",
  "schema:domainIncludes": [
    {
      "@id": "iscn:StakeholderInfo"
    }
  ],
  "schema:rangeIncludes": [
    {
      "@id": "schema:Number"
    }
  ]
}
```

## Sample

```json
95
```

## Description

| Property | Expected Type | Description                                   |
| -------- | ------------- | --------------------------------------------- |
| -        | Number        | Weighting of proportion expressed in a number |
