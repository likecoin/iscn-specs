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
The ISCN data model is composed of [linked data](#linked-data) from different data structures shown below:

![ISCN data model](https://gateway.pinata.cloud/ipfs/Qmacpqc7EWQBU9q8cctAj1hdoVXdyMH7Geq7FcpZ8XA5M8)

* [Meta](schema/meta/v1.md): The metadata on all of the ISCN data structures.
* [Entity](schema/entity/v1.md): The necessary information of an entity and all specific entity should inherit from [Entity](schema/entity/v1.md) to extend.
* [TimePeriod](schema/timeperiod/v1.md): The valid period of a life-cycle of an object.
* [ISCN](schema/iscn/v1.md): The core metadata that acts as a kernel of ISCN, and it connects the content itself, the stakeholders and the intellectual property rights with a unique global identifier.
* [Stakeholders](schema/stakeholders/v1.md): A list of [Stakeholder](schema/stakeholder/v1.md) and defines the ratio of profit sharing to each of the stakeholders.
* [Stakeholder](schema/stakeholder/v1.md): The information about the stakeholder, including the [Entity](schema/entity/v1.md) of the stakeholder and profit sharing ratio hint. Also, if the current digital work is a derivative work, then the source of underlying work is also registered as a creation footprint.
* [Rights](schema/rights/v1.md): A list of [Right](schema/right/v1.md) that describes the intellectual property rights.
* [Right](schema/right/v1.md): The information of the intellectual property rights granted by law, and it records that who is the holder, where and when the right applies and the detail of the terms of the right.
* [Content](schema/content/v1.md): The necessary metadata of digital content, including the fingerprint, the source location and the title & description of the digital content.

## Linked Data
Linked data is structured data that can be looked up via some methods, HTTP, RDF and URI but not limited to are all accepted.

## ISCN Architecture
The complete ISCN registration is consist of a kernel [ISCN](schema/iscn/v1.md) core metadata to record the unique global identifier and maintain the stakeholders, the intellectual property rights and the content metadata by [Stakeholder](schema/stakeholder/v1.md), [Rights](schema/rights/v1.md) and [Content](schema/content/v1.md) corresponsibly. The architecture of an ISCN is shown below:

![ISCN architecture](https://gateway.pinata.cloud/ipfs/QmbZGeySgjWPRA9dmFqnzUQe1xBU79yZ9pkHSCoqR9ou9j)

## ISCN content registry
A registry is a service provider for the ISCN registration, and a registry should provide service to register a digital content with metadata that follows the ISCN specification and to query. If any entities want to become a registry for ISCN, they should reserve a code for their registry in [here](https://github.com/likecoin/iscn-registry).

## ISCN Specification Guidelines
All contributors should create pull requests to propose the change of the specification. Contributors can post a proposal, and we call it ISCN Specification Proposal, abbreviated as ISP. For more detail about ISP, please check in [here](https://github.com/likecoin/iscn-specs/wiki/ISCN-Specification-Proposal).

## Contributing & Discussion
Suggestions, contributions, criticisms are welcome.
Discussion of specifications happens in [this repository's issues](https://github.com/likecoin/iscn-specs/issues) or via pull request.

## License
This repository is only for documents. All of these are licensed under the [CC-BY-SA 4.0 license](https://github.com/likecoin/iscn-specs/blob/master/LICENSE), © 2020 LikeCoin Foundation Ltd.
