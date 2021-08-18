# Content Metadata

The [Content Metadata](#) contains the necessary metadata of digital content, including the fingerprint, the source location and the name & description of the digital content.

## Schema

```json
{
  "@context": {
    "rdf": "http://www.w3.org/1999/02/22-rdf-syntax-ns#",
    "rdfs": "http://www.w3.org/2000/01/rdf-schema#",
    "schema": "https://schema.org/",
    "iscn": "http://iscn.io/"
  },
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
```

## Sample

```json
{
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
```

## Description

| Property      | Expected Type    | Description                                                                                                                                     |
| ------------- | ---------------- | ----------------------------------------------------------------------------------------------------------------------------------------------- |
| context       | URL              | The location of this schema: [http://schema.org/](http://schema.org/)                                                                           |
| type          | String           | The type of digital content. e.g. [CreativeWork](https://schema.org/CreativeWork) and its [subtypes](https://schema.org/CreativeWork#subtypes) |
| name         | String           | A name or a name of the digital content, and it recommends to keep in short.                                                                   |
| description   | String           | A brief description to introduce the digital content.                                                                                           |
| datePublished | String           | The timestamp of the creation or the modification of the ISCN record. It should be a human-readable DateTime and recommends to use ISO 8601.    |
| version       | Number           | Self defined version number                                                                                                                     |
| url           | String \| Object | The url of the creative work if exists                                                                                                          |
| author        | String \| Object | Author of the creative work                                                                                                                     |
| usageInfo     | String           | License or copyright information of the content                                                                                                 |
| keywords      | String           | A comma seperated list of keyword related to the content                                                                                        |
