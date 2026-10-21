# Maretha Labs

Practical software, AI integrations and developer tools from [Maretha](https://maretha.io).
We build applications and automated workflows around real business problems, and share
selected examples here so you can inspect the approach and the code.

Some projects are built with AI assistance; others integrate AI services or automate
specialist engineering work. Each repository explains its purpose, provenance, requirements
and validation limits. Public examples are not a promise of compatibility with every model
or a substitute for testing in your environment.

## Projects

| Project | What it demonstrates | Status |
| --- | --- | --- |
| [Operations Portal](https://github.com/maretha-labs/ops-portal) | A team interface for uploads, deployments, rollbacks, audit activity and logs. Built with Claude Code for Maretha's lab. | Existing public example |
| [Nuxeo upgrade assistant](https://github.com/maretha-labs/nuxeo-lts-2025-upgrade) | A Claude Code skill and references for LTS 2023 to 2025 project upgrades. | Skill and migration references; no version matrix certified |
| [Maretha AI](https://github.com/maretha-labs/maretha-ai) | Nuxeo interactions, metadata enrichment and retrieval with Bedrock and Vertesia integration code. | Source example; read security and validation notes |
| [MongoDB export transformer](https://github.com/maretha-labs/mongo-export-json-converter) | Streaming NDJSON transformation with explicit migration-specific mappings. | Tested utility example; not an AI runtime |
| [Nuxeo Admin Console](https://github.com/maretha-labs/nuxeo-admin-console) | A local single-page console for audit search and export, the management API, admin REST and Automation operations. | Built against LTS 2023 APIs; tested on macOS with Chrome |
| [Nuxeo Kafka Publisher](https://github.com/maretha-labs/nuxeo-kafka-publisher) | A Nuxeo add-on that publishes application messages to existing Kafka topics outside Nuxeo Stream, configured from `nuxeo.conf`. | `2025` branch (LTS 2025; LTS 2026 untested) and `2023` branch |
| [Fulltext extraction filter](https://github.com/maretha-labs/maretha-fulltext-filter) | A code example of how to adjust what goes into the fulltext index: extraction runs only for documents whose configured metadata value is allowlisted, instead of the standard selection by document type. | LTS 2023 with MongoDB only; re-test on each hotfix |
| [Nuxeo Expedited Delete](https://github.com/maretha-labs/nuxeo-expedited-delete) | A Nuxeo add-on bulk action that permanently deletes NXQL-matched documents as the system user, on its own stream; a commented guide to building bulk actions. | `2025` branch (LTS 2025); tested on H2 and in-memory storage, not MongoDB or Kafka |
| [Nuxeo Audit Forwarder](https://github.com/maretha-labs/nuxeo-audit-forwarder) | A Nuxeo add-on that forwards audit events to Splunk, IBM QRadar, Microsoft Sentinel, syslog, an HTTPS webhook and Amazon SQS, configured from `nuxeo.conf`. | `2025` branch (LTS 2025; LTS 2026 untested) and `2023` branch; not tested against real Splunk, QRadar or Sentinel |
| [Nuxeo MCP collaboration](https://github.com/maretha-labs/nuxeo-mcp-server) | MCP integration developed in collaboration with Hyland. | Labs reference fork; [Hyland maintains canonical source](https://github.com/nuxeo/nuxeo-mcp-server) |

## From example to your application

Have a repetitive task, a slow handoff or a process that takes too much of your team's time?
[Bring us your problem](https://maretha.io/contact). We can discuss the systems, model choices
and acceptance criteria needed for a useful solution.

## Releases and attribution

Each project is original Maretha work unless its README names another source. Collaboration
forks retain upstream provenance, copyright notices and applicable licenses. Tests and release
limits are documented per repository.

See the [release checklist](https://github.com/maretha-labs/.github/blob/main/RELEASING.md).
