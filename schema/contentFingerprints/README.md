# Entity

The [Entity](#) describes the necessary information of an entity, and all specific entity should inherit from [Entity](#) to extend.

## Schema

```json
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

| Property    | Occurs | Expected Type | Description                                                                                                                   |
| ----------- | ------ | ------------- | ----------------------------------------------------------------------------------------------------------------------------- |
