# International Standard Content Number Specifications

The goal of International Standard Content Number, abbreviated as ISCN, is to create a fundamental schema for a digital content registration. The ISCN is a cornerstone to build a global, decentralised and resilient digital content registry. This schema helps to identify a specific digital content, records the content metadata, the intellectual property rights and the stakeholders of the creation.

## ISCN Goals

The target of ISCN is to build a general digital content registration schema, and it should satisfy the following:

1. Every ISCN has a unique global identifier
1. All Changes of the metadata must be traceable
1. The schema must be extensible
1. Registering content fingerprint of the digital content
1. Linking the all creation components as a creation footprint
1. Connecting the digital content to the corresponding intellectual property rights
1. Associating the stakeholders of the digital content and providing a hint for profit sharing

## ISCN Data Model

The ISCN data model is composed of [linked data](#linked-data) from different data structures shown below. ISCN data is [JSON-LD](https://json-ld.org/) compatible:

![ISCN data model](https://gateway.pinata.cloud/ipfs/Qmacpqc7EWQBU9q8cctAj1hdoVXdyMH7Geq7FcpZ8XA5M8)

- [contentMetadata](schema/contentMetadata/README.md): Basic content metadata.
- [footprint](schema/footprint/README.md): Referring to other contents (e.g. citation or derivative works)
- [recordNotes](schema/recordNotes/README.md): Brief description of a content.
- [recordVersion](schema/recordVersion/README.md): Version of the ISCN record, independent of the content version.
- [StakeholderInfo](schema/StakeholderInfo/README.md): Information of a entity who/which contributed to the content, and its weighting.
- [contributionType](schema/contributionType/README.md): Type of the contribution of a StakeholderInfo
- [ISCN Record](schema/record/README.md): The core metadata that acts as a kernel of ISCN, and it connects the content itself, the stakeholders, the fingerprints and other relevant metadata with a unique global identifier.
- [recordParentIPLD](schema/recordParentIPLD/README.md): The IPLD hash of the previous version of this record.
- [rewardProportion](schema/rewardProportion/README.md): The suggested reward propotion of a stakeholder.
- [contentFingerprints](schema/contentFingerprints/README.md): Fingerprints of the content, e.g. cryptographic hashe, URI, etc.
- [entity](schema/entity/README.md): Entity who should be cited and / or rewarded for the contribution on the content.
- [recordTimestamp](schema/recordTimestamp/README.md): The timestamp of the current version of the ISCN record.
- [stakeholders](schema/stakeholders/README.md): List of StakeholderInfo contributed to this content.

A full list of schema can be found at [schema](https://github.com/likecoin/iscn-specs/tree/master/schema), and ISCN record samples can be found in [here](https://github.com/likecoin/iscn-specs/tree/develop/sample).

## Linked Data

Linked data is structured data that can be looked up via some methods, HTTP, RDF and URI but not limited to are all accepted.

## ISCN Architecture

The complete ISCN registration is consist of a kernel [ISCN](schema/iscn.md) record to record the unique global identifier and maintain the stakeholders, and the content metadata by [stakeholders](schema/stakeholders/README.md), [contentFingerprints](schema/contentFingerprints/README.md) and [contentMetadata](schema/contentMetadata/README.md) corresponsibly. Other metadata can be added flexiblely through [JSON-LD](https://json-ld.org/) and [schema.org](https://schema.org/) standard. The basic architecture of an ISCN is shown below:

![ISCN architecture](https://gateway.pinata.cloud/ipfs/QmT3gD8KvowzpaU2n4ppc7EHnJ7rgqkbRCqgKmdvYHSTiv)

## ISCN content registry

A registry is a service provider for the ISCN registration, and a registry should provide service to register a digital content with metadata that follows the ISCN specification and to query. If any entities want to become a registry for ISCN, they should reserve a code for their registry in [here](https://github.com/likecoin/iscn-registry-index).

## ISCN Specification Guidelines

All contributors should create pull requests to propose the change of the specification. Contributors can post a proposal, and we call it ISCN Specification Proposal, abbreviated as ISP. For more detail about ISP, please check in [here](https://github.com/likecoin/iscn-specs/wiki/ISCN-Specification-Proposal).

## Contributing & Discussion

Suggestions, contributions, criticisms are welcome.
Discussion of specifications happens in [this repository's issues](https://github.com/likecoin/iscn-specs/issues) or via pull request.

## License

This repository is only for documents. All of these are licensed under the [CC-BY-SA 4.0 license](https://github.com/likecoin/iscn-specs/blob/master/LICENSE), � 2020 LikeCoin Foundation Ltd.
