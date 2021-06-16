# Content FingerPrints

The [Content FingerPrints](#) is the fingerprints of the content, e.g. cryptographic hashes of content files. To be complete, there could be more than one fingerprint, so this field should be presented as a list of fingerprints. For interoperability, the fingerprints should be encoded in IRI (URI) format, e.g. hash URI (https://github.com/hash-uri/hash-uri)

## Schema

```json
{
  "@context": {
    "rdf": "http://www.w3.org/1999/02/22-rdf-syntax-ns#",
    "rdfs": "http://www.w3.org/2000/01/rdf-schema#",
    "schema": "https://schema.org/",
    "iscn": "http://iscn.io/"
  },
  "@id": "iscn:contentFingerprints",
  "@type": "rdf:Property",
  "rdfs:comment": "Fingerprints of the content, e.g. cryptographic hashes of content files. To be complete, there could be more than one fingerprint, so this field should be presented as a list of fingerprints. For interoperability, the fingerprints should be encoded in IRI (URI) format, e.g. hash URI (https://github.com/hash-uri/hash-uri).",
  "rdfs:label": "contentFingerprints",
  "schema:domainIncludes": [
    {
      "@id": "iscn:Record"
    }
  ]
}
```

## Sample

```json
[
    "hash://sha256/9564b85669d5e96ac969dd0161b8475bbced9e5999c6ec598da718a3045d6f2e",
    "ipfs://QmNrgEMcUygbKzZeZgYFosdd27VE9KnWbyUD73bKZJ3bGi",
],
```

## Description

| Property | Expected Type | Description                                                                          |
| -------- | ------------- | ------------------------------------------------------------------------------------ |
| -        | String[]      | List of URI of the content, e.g. hash://, ipfs://, https://, or other applicable URI |
