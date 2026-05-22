# AsyncAPI

Topic index for the **AsyncAPI** ecosystem — the open specification, tooling, and adopter community for describing event-driven and message-driven APIs. AsyncAPI is to asynchronous APIs what OpenAPI is to synchronous REST: a machine-readable contract describing channels, operations, messages, servers, and protocol bindings.

**Type:** Topic Index
**Specification:** [asyncapi.com/docs/reference/specification/latest](https://www.asyncapi.com/docs/reference/specification/latest)
**Source:** [github.com/asyncapi/spec](https://github.com/asyncapi/spec)
**Governance:** [AsyncAPI Project — a Series of LF Projects, LLC](https://www.linuxfoundation.org/projects)
**Latest version:** **3.1.0** (January 2026) — adds ROS 2 bindings
**Previous major:** **3.0.0** (December 2023) — channels/operations separation

## What AsyncAPI Is

AsyncAPI is a YAML or JSON contract describing an event-driven application. The root document contains:

- `info` — title, version, description, contact, license
- `servers` — broker(s) the app connects to (Kafka, MQTT, AMQP, NATS, WebSocket, SNS, SQS, JMS, Pulsar, IBM MQ, Google Pub/Sub, ROS 2, HTTP)
- `channels` — addressable message endpoints (Kafka topic, MQTT topic filter, AMQP exchange/queue, WebSocket path, NATS subject)
- `operations` — `send` or `receive` actions the application performs on a channel (first-class in 3.0+)
- `components` — reusable schemas, messages, security schemes, parameters, traits, bindings, correlation IDs, replies

The 3.0 release in December 2023 broke compatibility by lifting operations out of channels and making them top-level objects — enabling cleaner reuse of channels across multiple operations and richer request/reply modelling.

## AsyncAPI vs OpenAPI

| | OpenAPI | AsyncAPI |
|---|---|---|
| **Paradigm** | Request/response (HTTP) | Event-driven / message-driven |
| **Top-level** | `paths` + `operations` | `channels` + `operations` |
| **Addressable unit** | URL path | Channel address (topic, queue, subject) |
| **Action vocabulary** | HTTP method (GET/POST/...) | `send` / `receive` |
| **Servers** | One protocol (HTTP) | 14+ protocols via bindings |
| **Status** | OpenAPI 3.1 (CNCF / OAI) | AsyncAPI 3.1 (LF) |

AsyncAPI deliberately reuses much of the OpenAPI design language (info, components, $ref, JSON Schema for payloads) so teams can adopt it without learning a new mental model.

## Artifacts

### JSON Schemas
- [asyncapi-document-schema.json](json-schema/asyncapi-document-schema.json) — Root AsyncAPI document
- [asyncapi-channel-schema.json](json-schema/asyncapi-channel-schema.json) — Channel object
- [asyncapi-operation-schema.json](json-schema/asyncapi-operation-schema.json) — Operation object (3.0+ top-level)
- [asyncapi-message-schema.json](json-schema/asyncapi-message-schema.json) — Message object
- [asyncapi-server-schema.json](json-schema/asyncapi-server-schema.json) — Server object

### JSON-LD Context
- [async-apis-context.jsonld](json-ld/async-apis-context.jsonld) — Linked-data context mapping AsyncAPI terms

### Vocabulary
- [async-apis-vocabulary.yml](vocabulary/async-apis-vocabulary.yml) — Normative AsyncAPI terminology (32 terms)

### Example Documents
- [asyncapi-kafka-example.yml](examples/asyncapi-kafka-example.yml) — User signup event stream over Apache Kafka (kafka-secure, CloudEvents payload, schema registry)
- [asyncapi-mqtt-example.yml](examples/asyncapi-mqtt-example.yml) — IoT thermostat telemetry over MQTT 5 (last will, parameterized channels, QoS bindings)
- [asyncapi-websocket-example.yml](examples/asyncapi-websocket-example.yml) — Live market quotes over WebSocket (subscribe/unsubscribe with reply pattern)

## Protocol Bindings

AsyncAPI is protocol-neutral; bindings are versioned independently and live in [`asyncapi/bindings`](https://github.com/asyncapi/bindings):

| Protocol | Typical use | Server binding | Operation binding | Message binding |
|---|---|---|---|---|
| **Kafka** | Event streaming | schema registry url/vendor | groupId, clientId | key, schemaId* |
| **MQTT** | IoT telemetry | clientId, lastWill, keepAlive | qos, retain | payloadFormatIndicator, contentType |
| **AMQP 0.9.1** | Enterprise messaging (RabbitMQ) | — | expiration, priority, deliveryMode | — |
| **WebSocket** | Browser push, live data | — | method, query, headers | — |
| **NATS** | Lightweight pub/sub | — | queue (group) | — |
| **SNS** | AWS fan-out | — | ordering, deduplication | — |
| **SQS** | AWS work queues | — | redrive policy, FIFO | — |
| **JMS** | Java enterprise | destination | priority, deliveryMode | — |
| **Pulsar** | Event streaming | tenant, namespace | — | — |
| **IBM MQ** | Enterprise messaging | queueManager | expiry, persistence | — |
| **Google Pub/Sub** | GCP messaging | topic | — | orderingKey |
| **ROS 2** | Robotics middleware (new in 3.1) | — | — | — |
| **HTTP** | Webhooks | — | method | headers schema |

## Tooling Landscape

### Official AsyncAPI Org
- **[Studio](https://studio.asyncapi.com/)** — Browser-based visual editor with live preview
- **[Parser](https://github.com/asyncapi/parser-js)** — JS + Go validators, shared parser-api
- **[Modelina](https://modelina.org/)** — Typed model generation in 11+ languages
- **[Generator](https://github.com/asyncapi/generator)** — Template-driven anything generator
- **[CLI](https://github.com/asyncapi/cli)** — `validate`, `generate`, `convert` 2.x→3.x, `bundle`, `new`
- **[React Component](https://github.com/asyncapi/asyncapi-react)** — HTML doc rendering used by Studio
- **[Glee](https://github.com/asyncapi/glee)** — Spec-first Node.js application framework

### Code-First Frameworks
- **[Springwolf](https://www.springwolf.dev/)** — Spring Boot @KafkaListener / @RabbitListener / @JmsListener auto-gen
- **[FastStream](https://faststream.airt.ai/)** — Python framework (Kafka, RabbitMQ, NATS, Redis Pub/Sub)
- **[nestjs-asyncapi](https://github.com/flamewow/nestjs-asyncapi)** — NestJS decorators
- **[AsyncAPI.NET](https://github.com/LEGO/AsyncAPI.NET)** — C#/.NET code-first

### Mocking / Contract Testing
- **[Microcks](https://microcks.io/)** — CNCF Sandbox, Kubernetes-native; mocks Kafka, MQTT, AMQP, WebSocket, NATS, SNS, SQS, Google Pub/Sub, IBM MQ
- **[Mokapi](https://mokapi.io/)** — Go-based with visual dashboard
- **[Virtualan](https://virtualan.io/)** — Kubernetes-native

### Schema Registry
- **[Apicurio Registry](https://www.apicur.io/registry/)** — Red Hat OSS; stores AsyncAPI alongside Avro, Protobuf, JSON Schema, OpenAPI

### Linting / Quality
- **[Spectral](https://stoplight.io/open-source/spectral)** — AsyncAPI 2.x linting rulesets

## Notable Adopters

The AsyncAPI [case studies](https://www.asyncapi.com/casestudies) page documents:

- **Adeo** (Leroy Merlin parent) — Standardised API documentation across the group
- **HDI Global SE** — System-wide communication overview
- **TransferGo** — Spec-as-blueprint for event-driven microservices

Public adoption beyond case studies includes Adidas, Mercado Libre, Walmart, eBay, LEGO Group, Salesforce, Raiffeisen Bank, Postman, and SAP — published in blog posts, conference talks, and GitHub orgs.

## Specification Version History (Selected)

| Version | Date | Highlights |
|---|---|---|
| **3.1.0** | January 2026 | ROS 2 bindings added to official spec |
| **3.0.1** | December 2023 | Library update; no spec changes |
| **3.0.0** | December 2023 | Major restructure — operations split from channels; Reply object; new Components types |
| **2.6.0** | October 2022 | Last 2.x line release |
| **2.0.0** | September 2020 | Major rewrite; modern JSON Schema |
| **1.0.0** | August 2017 | Initial public release |

## Why This Matters

Synchronous request/response APIs got OpenAPI and an entire industry of tooling. The asynchronous half of the modern stack — Kafka topics, MQTT telemetry, AMQP queues, WebSocket streams, NATS subjects, SNS fan-outs — was effectively undocumented until AsyncAPI. The 3.0 release brought the spec to maturity by cleanly separating channel definition (where messages live) from operation declaration (what this application does on that channel) — finally letting publishers, subscribers, and contract-test tools share one document.

## Related API Evangelist Repos

- [`asyncapi`](https://github.com/api-evangelist/asyncapi) — Standard repo for the spec itself
- [`events`](https://github.com/api-evangelist/events) — General event-driven topic
- [`streaming`](https://github.com/api-evangelist/streaming) — Streaming APIs topic
- [`websockets`](https://github.com/api-evangelist/websockets) — WebSocket protocol topic
- [`kafka`](https://github.com/api-evangelist/kafka) — Apache Kafka topic
- [`messaging-api`](https://github.com/api-evangelist/messaging-api) — Messaging API topic
- [`messaging-protocol`](https://github.com/api-evangelist/messaging-protocol) — Messaging protocols topic

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
