# Content Metadata

The [Content Metadata](#) contains the necessary metadata of digital content, including the fingerprint, the source location and the title & description of the digital content.

## Schema

```json
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
```

## Sample

```json
{
  "@context": "http://schema.org/",
  "@type": "CreativeWorks",
  "title": "使用矩陣計算遞歸關係式",
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

| Property    | Occurs           | Expected Type       | Description                                                                                                                                                                                                                                                                                                                                                                                          |
| ----------- | ---------------- | ------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| context     | 1                | URL                 | The location of this schema:<br>[https://iscn.io/schema/content-v1](https://iscn.io/schema/content-v1)                                                                                                                                                                                                                                                                                               |
| type        | 1                | String              | The type of digital content. The specific type of digital content should define this value.                                                                                                                                                                                                                                                                                                          |
| version     | 1                | Number              | Once the content metadata is registered, the version counts as **1**. When there is any update later, the version number will go up one by one.                                                                                                                                                                                                                                                      |
| parent      | 0<sup>\*</sup>~1 | [<u>Content</u>](#) | A [linked data](../../README.md#linked-data) to the previous version of the content metadata.<br><br>_\* Only if the version is **1**, otherwise parent must be linked._                                                                                                                                                                                                                             |
| source      | 0~1              | URL                 | An URL to locate the source of digital content.                                                                                                                                                                                                                                                                                                                                                      |
| edition     | 0~1              | String              | The edition of digital content. It can be any kind of string that the creator to choose.                                                                                                                                                                                                                                                                                                             |
| fingerprint | 1                | String \| Object    | The fingerprint of digital content. The ISCN registry should define the precise algorithm used for each type of digital content. For example, it can be a particular cryptographic hash operation on the source file of the digital content or any newly defined data structure for the specific type of content. The chosen algorithm requires that it is a cryptographically strong hash function. |
| feature     | 0~1              | String \| Object    | The `feature` is another fingerprint of content, which, unlike the cryptographic fingerprint, does not apply to the specific encoding of the file. Instead, it extracts the features of the content by some content-specific characteristics. For example, the feature field of an article could be an encoded vector of the keywords of that article.                                               |
| title       | 1                | String              | A title or a name of the digital content, and it recommends to keep in short.                                                                                                                                                                                                                                                                                                                        |
| description | 0~1              | String              | A brief description to introduce the digital content.                                                                                                                                                                                                                                                                                                                                                |
| tags        | 0~1              | [String]            | A list of hashtags/keywords of the digital content.                                                                                                                                                                                                                                                                                                                                                  |
