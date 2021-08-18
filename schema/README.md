# ISCN schema

## JSONLD schema

```json
{
  "@context": {
    "rdf": "http://www.w3.org/1999/02/22-rdf-syntax-ns#",
    "rdfs": "http://www.w3.org/2000/01/rdf-schema#",
    "schema": "https://schema.org/",
    "iscn": "http://iscn.io/"
  },
  "@graph": [
    {
      "@id": "iscn:Record",
      "@type": "rdfs:Class",
      "rdfs:comment": "An ISCN record, recording the metadata of the content. The registry generating this record should create a unique identifier (the ISCN ID) for this record.",
      "rdfs:label": "Record",
      "rdfs:subClassOf": {
        "@id": "schema:Thing"
      }
    },
    {
      "@id": "iscn:recordTimestamp",
      "@type": "rdf:Property",
      "rdfs:comment": "The timestamp of the current version of the ISCN record, recorded by the registry, in ISO 8601 format.",
      "rdfs:label": "recordTimestamp",
      "schema:domainIncludes": [
        {
          "@id": "iscn:Record"
        }
      ],
      "schema:rangeIncludes": [
        {
          "@id": "schema:DateTime"
        }
      ]
    },
    {
      "@id": "iscn:recordVersion",
      "@type": "rdf:Property",
      "rdfs:comment": "The version of the ISCN record. It could be different from the content's version, as one may update only the content metadata or ISCN record fields without modifying the content itself.",
      "rdfs:label": "recordVersion",
      "schema:domainIncludes": [
        {
          "@id": "iscn:Record"
        }
      ],
      "schema:rangeIncludes": [
        {
          "@id": "schema:Number"
        }
      ]
    },
    {
      "@id": "iscn:recordNotes",
      "@type": "rdf:Property",
      "rdfs:comment": "A summary on the current record version, similar to Git commit logs.",
      "rdfs:label": "recordNotes",
      "schema:domainIncludes": [
        {
          "@id": "iscn:Record"
        }
      ],
      "schema:rangeIncludes": [
        {
          "@id": "schema:Text"
        }
      ]
    },
    {
      "@id": "iscn:recordParentIPLD",
      "@type": "rdf:Property",
      "rdfs:comment": "The IPLD hash of the previous version of this record, if any. For interoperability, it should fulfill the DAG-JSON IPLD codec, i.e. be an object containing a `/` key associated with a string value, which is the Base32 encoding of the CID of the parent record.",
      "rdfs:label": "recordParentIPLD",
      "schema:domainIncludes": [
        {
          "@id": "iscn:Record"
        }
      ]
    },
    {
      "@id": "iscn:contentFingerprints",
      "@type": "rdf:Property",
      "rdfs:comment": "Fingerprints of the content, e.g. cryptographic hashes of content files. To be complete, there could be more than one fingerprint, so this field should be presented as a list of fingerprints. For interoperability, the fingerprints should be encoded in IRI (URI) format, e.g. hash URI (https://github.com/hash-uri/hash-uri).",
      "rdfs:label": "contentFingerprints",
      "schema:domainIncludes": [
        {
          "@id": "iscn:Record"
        }
      ]
    },
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
    },
    {
      "@id": "iscn:StakeholderInfo",
      "@type": "rdfs:Class",
      "rdfs:comment": "One entry of the stakeholder list of the content, describing who or which content should be cited for the contribution to the content, and how much should the contribution be rewarded.",
      "rdfs:label": "StakeholderInfo",
      "rdfs:subClassOf": {
        "@id": "schema:Thing"
      }
    },
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
    },
    {
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
    },
    {
      "@id": "iscn:contributionType",
      "@type": "rdf:Property",
      "rdfs:comment": "The type of the contribution. For interoperability, users are encouraged to use existing schema IRIs (e.g. http://schema.org/author, http://schema.org/publisher, http://schema.org/citation, http://schema.org/isBasedOn, http://schema.org/hasPart) for this field.",
      "rdfs:label": "contributionType",
      "schema:domainIncludes": [
        {
          "@id": "iscn:StakeholderInfo"
        }
      ]
    },
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
    },
    {
      "@id": "iscn:contentMetadata",
      "@type": "rdf:Property",
      "rdfs:comment": "The content metadata. For schema, http://schema.org/CreativeWork is recommended.",
      "rdfs:label": "contentMetadata",
      "schema:domainIncludes": [
        {
          "@id": "schema:CreativeWork"
        }
      ]
    }
  ]
}
```

## Sample ISCN entry

```json
{
  "@context": {
    "@vocab": "http://iscn.io/",
    "recordParentIPLD": {
      "@container": "@index"
    },
    "stakeholders": {
      "@context": {
        "@vocab": "http://schema.org/",
        "entity": "http://iscn.io/entity",
        "rewardProportion": "http://iscn.io/rewardProportion",
        "contributionType": "http://iscn.io/contributionType",
        "footprint": "http://iscn.io/footprint"
      }
    },
    "contentMetadata": {
      "@context": null
    }
  },
  "@type": "Record",
  "@id": "iscn://likecoin-chain/btC7CJvMm4WLj9Tau9LAPTfGK7sfymTJW7ORcFdruCU/2",
  "recordTimestamp": "2021-03-23T12:00:00+08:00",
  "recordVersion": 2,
  "recordNotes": "Add IPFS fingerprint",
  "recordParentIPLD": {
    "/": "bahuaierav3bfvm4ytx7gvn4yqeu4piiocuvtvdpyyb5f6moxniwemae4tjyq"
  },
  "contentFingerprints": [
    "hash://sha256/9564b85669d5e96ac969dd0161b8475bbced9e5999c6ec598da718a3045d6f2e",
    "ipfs://QmNrgEMcUygbKzZeZgYFosdd27VE9KnWbyUD73bKZJ3bGi"
  ],
  "stakeholders": [
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
  ],
  "contentMetadata": {
    "@context": "http://schema.org/",
    "@type": "Article",
    "name": "使用矩陣計算遞歸關係式",
    "description": "An article on computing recursive function with matrix multiplication.",
    "datePublished": "2019-04-19",
    "version": 1,
    "url": "https://nnkken.github.io/post/recursive-relation/",
    "author": "https://github.com/nnkken",
    "usageInfo": "https://creativecommons.org/licenses/by/4.0",
    "keywords": "matrix,recursion"
  }
}
```
