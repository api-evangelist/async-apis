# AsyncAPI (async-apis)

Topic index for the AsyncAPI ecosystem — the open specification, tooling, and adopter community for describing event-driven and message-driven APIs. AsyncAPI is to asynchronous APIs what OpenAPI is to synchronous REST: a machine-readable contract describing channels, operations, messages, servers, and protocol bindings (Kafka, MQTT, AMQP, WebSocket, NATS, SNS, SQS, JMS, Pulsar, IBM MQ, ROS 2, and more). This repo catalogs the specification versions, the canonical tooling (Studio, Parser, Modelina, Generator, CLI), validators (Spectral, Microcks, Apicurio Registry), code-first frameworks (Springwolf, FastStream, nestjs-asyncapi, AsyncAPI.NET), and real-world adopters (Adeo, HDI Global, TransferGo, Walmart, LEGO, eBay, Salesforce).

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/async-apis/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/async-apis/refs/heads/main/apis.yml)

## Scope

- **Type:** Index

## Tags

- AsyncAPI
- Event-Driven Architecture
- Asynchronous APIs
- Message Brokers
- API Specifications
- Kafka
- MQTT
- AMQP
- WebSocket
- Linux Foundation

## Timestamps

- **Created:** 2026-05-22
- **Modified:** 2026-05-22

## APIs

### AsyncAPI Specification

The AsyncAPI Specification is an open-source machine-readable format for describing asynchronous APIs. It defines channels (the addressable message endpoints), operations (send/receive actions an application performs), messages (the payload schema), servers (the broker connection details), and bindings (protocol-specific details for Kafka, MQTT, AMQP, WebSocket, NATS, SNS, SQS, and others). Version 3.0 (December 2023) introduced a major restructuring separating operations from channels; version 3.1.0 (January 2026) added ROS 2 bindings.

- **Human URL:** [https://www.asyncapi.com/](https://www.asyncapi.com/)
- **Base URL:** `https://www.asyncapi.com/`

#### Tags

- Specification
- Event-Driven Architecture
- Linux Foundation

#### Properties

- [Website](https://www.asyncapi.com/)
- [Documentation](https://www.asyncapi.com/docs)
- [Specification](https://www.asyncapi.com/docs/reference/specification/latest)
- [Specification Repo](https://github.com/asyncapi/spec)
- [Releases](https://github.com/asyncapi/spec/releases)
- [JSON Schema](https://github.com/asyncapi/spec-json-schemas) — [JSON Schema](https://json-schema.org/specification)
- [Blog](https://www.asyncapi.com/blog)
- [Newsroom](https://www.asyncapi.com/community/newsroom)
- [Case Studies](https://www.asyncapi.com/casestudies)
- [Governance](https://github.com/asyncapi/community)
- [Slack](https://www.asyncapi.com/slack-invite)
- [GitHub Organization](https://github.com/asyncapi)
- [Postman Collection](collections/async-apis.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/async-apis.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### AsyncAPI Studio

AsyncAPI Studio is the official browser-based editor for visually designing AsyncAPI documents and event-driven architectures. It provides a real-time preview rendered by the AsyncAPI React component, validation via the AsyncAPI Parser, and example generation for messages.

- **Human URL:** [https://studio.asyncapi.com/](https://studio.asyncapi.com/)

#### Tags

- Editor
- Studio
- Tooling

#### Properties

- [Website](https://studio.asyncapi.com/)
- [Git Hub](https://github.com/asyncapi/studio)
- [Documentation](https://www.asyncapi.com/tools/studio)
- [Postman Collection](collections/async-apis.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/async-apis.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### AsyncAPI Parser

The AsyncAPI Parser parses, validates, and provides a programmatic API over AsyncAPI documents. It is the reference implementation used by Studio, the CLI, and the Generator. Available in JavaScript and Go; a shared parser-api defines the interface.

- **Human URL:** [https://github.com/asyncapi/parser-js](https://github.com/asyncapi/parser-js)

#### Tags

- Parser
- Validator
- Tooling

#### Properties

- [Parser J S](https://github.com/asyncapi/parser-js)
- [Parser Go](https://github.com/asyncapi/parser-go)
- [Parser A P I](https://github.com/asyncapi/parser-api)
- [N P M](https://www.npmjs.com/package/@asyncapi/parser)
- [Postman Collection](collections/async-apis.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/async-apis.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### AsyncAPI Modelina

Modelina is the AsyncAPI library for generating typed payload models from AsyncAPI, OpenAPI, JSON Schema, and Avro documents. Supports Java, TypeScript, JavaScript, Go, C#, Rust, Python, Kotlin, Dart, PHP, and C++ output with high customization.

- **Human URL:** [https://modelina.org/](https://modelina.org/)

#### Tags

- Code Generation
- Modeling
- Tooling

#### Properties

- [Website](https://modelina.org/)
- [Git Hub](https://github.com/asyncapi/modelina)
- [Playground](https://modelina.org/playground)
- [Postman Collection](collections/async-apis.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/async-apis.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### AsyncAPI Generator

The AsyncAPI Generator takes an AsyncAPI document plus a template and generates anything — markdown docs, HTML, Node.js code, Python code, Java code, AMQP/MQTT/Kafka clients. Template registry includes html-template, markdown-template, nodejs-template, java-template, python-paho-template, ts-nats-template.

- **Human URL:** [https://github.com/asyncapi/generator](https://github.com/asyncapi/generator)

#### Tags

- Code Generation
- Documentation
- Tooling

#### Properties

- [Git Hub](https://github.com/asyncapi/generator)
- [N P M](https://www.npmjs.com/package/@asyncapi/generator)
- [Templates](https://github.com/asyncapi/template-for-generator-templates)
- [Postman Collection](collections/async-apis.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/async-apis.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### AsyncAPI CLI

The AsyncAPI CLI is the unified command-line interface for the AsyncAPI ecosystem. Commands include `validate`, `generate`, `optimize`, `convert` (2.x to 3.x), `new` (scaffold a spec), `bundle`, and `start studio`.

- **Human URL:** [https://github.com/asyncapi/cli](https://github.com/asyncapi/cli)

#### Tags

- CLI
- Tooling

#### Properties

- [Git Hub](https://github.com/asyncapi/cli)
- [N P M](https://www.npmjs.com/package/@asyncapi/cli)
- [Documentation](https://www.asyncapi.com/tools/cli)
- [Postman Collection](collections/async-apis.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/async-apis.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### AsyncAPI React Component

The AsyncAPI React component renders interactive HTML documentation from an AsyncAPI document. Used by Studio, html-template, and the asyncapi-react Storybook playground. Also available as a Web Component.

- **Human URL:** [https://github.com/asyncapi/asyncapi-react](https://github.com/asyncapi/asyncapi-react)

#### Tags

- Documentation
- React
- Tooling

#### Properties

- [Git Hub](https://github.com/asyncapi/asyncapi-react)
- [N P M](https://www.npmjs.com/package/@asyncapi/react-component)
- [Postman Collection](collections/async-apis.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/async-apis.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Microcks

Microcks is a Kubernetes-native open-source platform for API mocking and contract testing. First-class support for AsyncAPI — it consumes AsyncAPI documents and stands up mock Kafka, MQTT, AMQP, WebSocket, NATS, SNS, SQS, Google PubSub, and IBM MQ endpoints replaying example messages from the contract.

- **Human URL:** [https://microcks.io/](https://microcks.io/)

#### Tags

- Mocking
- Contract Testing
- CNCF
- Tooling

#### Properties

- [Website](https://microcks.io/)
- [Git Hub](https://github.com/microcks/microcks)
- [Documentation](https://microcks.io/documentation/)
- [Async A P I Support](https://microcks.io/documentation/explanations/asyncapi-support/)
- [C N C F Sandbox](https://www.cncf.io/projects/microcks/)
- [Postman Collection](collections/async-apis.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/async-apis.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Apicurio Registry

Apicurio Registry is an open-source schema and API registry from Red Hat that stores AsyncAPI, OpenAPI, JSON Schema, Avro, Protobuf, GraphQL, and XML Schema artifacts. Integrates with Kafka, Kafka Connect, and Kafka Streams via SerDes libraries, and enforces compatibility rules on schema evolution.

- **Human URL:** [https://www.apicur.io/registry/](https://www.apicur.io/registry/)

#### Tags

- Schema Registry
- Registry
- Tooling

#### Properties

- [Website](https://www.apicur.io/registry/)
- [Git Hub](https://github.com/Apicurio/apicurio-registry)
- [Documentation](https://www.apicur.io/registry/docs/)
- [Postman Collection](collections/async-apis.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/async-apis.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Springwolf

Springwolf is the code-first AsyncAPI generator for Spring Boot applications. It auto-detects @KafkaListener, @RabbitListener, @JmsListener, @SqsListener, @SnsListener, and Cloud Stream bindings and produces an AsyncAPI document plus an interactive UI at runtime.

- **Human URL:** [https://www.springwolf.dev/](https://www.springwolf.dev/)

#### Tags

- Code-First
- Spring Boot
- Tooling

#### Properties

- [Website](https://www.springwolf.dev/)
- [Git Hub](https://github.com/springwolf/springwolf-core)
- [Postman Collection](collections/async-apis.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/async-apis.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### FastStream

FastStream is a Python framework that auto-generates AsyncAPI documentation from typed message handlers for Kafka, RabbitMQ, NATS, Redis Pub/Sub, and Confluent Kafka. Created by airtai and donated to the AsyncAPI community.

- **Human URL:** [https://faststream.airt.ai/](https://faststream.airt.ai/)

#### Tags

- Code-First
- Python
- Tooling

#### Properties

- [Website](https://faststream.airt.ai/)
- [Git Hub](https://github.com/airtai/faststream)
- [Postman Collection](collections/async-apis.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/async-apis.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Glee

Glee is the AsyncAPI-native application framework. It takes an AsyncAPI document as input and scaffolds a working server (Node.js) that handles the channels, validates messages against the schema, and routes them to user-supplied handler functions.

- **Human URL:** [https://github.com/asyncapi/glee](https://github.com/asyncapi/glee)

#### Tags

- Framework
- Application Server
- Tooling

#### Properties

- [Git Hub](https://github.com/asyncapi/glee)
- [Postman Collection](collections/async-apis.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/async-apis.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

## Common Properties

- [Topic Index](https://github.com/api-evangelist/async-apis)
- [JSON Schema](json-schema/asyncapi-document-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Schema](json-schema/asyncapi-channel-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Schema](json-schema/asyncapi-operation-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Schema](json-schema/asyncapi-message-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Schema](json-schema/asyncapi-server-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON-LD](json-ld/async-apis-context.jsonld) — [JSON-LD](https://www.w3.org/TR/json-ld11/)
- [Vocabulary](vocabulary/async-apis-vocabulary.yml)
- [Examples](examples/asyncapi-kafka-example.yml)
- [Examples](examples/asyncapi-mqtt-example.yml)
- [Examples](examples/asyncapi-websocket-example.yml)
- [Specification](https://www.asyncapi.com/docs/reference/specification/latest)
- [Specification Repo](https://github.com/asyncapi/spec)
- [GitHub Organization](https://github.com/asyncapi)
- [Governance](https://github.com/asyncapi/community)
- [Linux Foundation Project](https://www.linuxfoundation.org/projects)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
