# Salesforce Service Cloud GraphQL Schema

## Overview

This conceptual GraphQL schema represents the Salesforce Service Cloud data model, derived from the Salesforce REST API, Live Agent REST API, and associated developer documentation. It covers the core objects and relationships used in customer service operations including case management, contact and account management, knowledge base, live chat, omni-channel routing, surveys, and automation flows.

**Source APIs:**
- [Salesforce REST API](https://developer.salesforce.com/docs/atlas.en-us.api_rest.meta/api_rest/)
- [Live Agent REST API](https://developer.salesforce.com/docs/atlas.en-us.live_agent_rest.meta/live_agent_rest/)
- [Knowledge API](https://developer.salesforce.com/docs/atlas.en-us.knowledge_dev.meta/knowledge_dev/)
- [Omni-Channel API](https://developer.salesforce.com/docs/atlas.en-us.omni_channel_dev.meta/omni_channel_dev/omnichannel_developer_guide_intro.htm)

## Schema Organization

The schema is organized into the following functional domains:

### Case Management
Core types for tracking customer issues and support requests:
- `Case`, `CaseDetails`, `CaseStatus`, `CasePriority`, `CaseOrigin`, `CaseType`, `CaseReason`, `CaseSubject`
- `CaseComment`, `CaseFeed`, `EmailMessage`, `CaseEmailMessage`
- `TaskRecord`, `ActivityHistory`

### Contact and Account Management
Types for managing customer relationships:
- `Contact`, `ContactDetails`
- `Account`, `AccountDetails`
- `EntitlementContact`, `Entitlement`, `EntitlementDetails`
- `ServiceContract`, `ServiceContractLine`, `ContractLine`, `OrderItem`
- `Milestone`, `MilestoneCriteria`

### Agent and Queue Management
Types for workforce and routing management:
- `AgentWork`, `AgentDetails`
- `Queue`, `QueueMember`

### Live Chat
Types for real-time customer chat sessions:
- `LiveChat`, `ChatSession`, `ChatMessage`, `ChatTranscript`
- `Visitor`, `VisitorDetails`

### Knowledge Base
Types for managing help content and articles:
- `Article`, `KnowledgeArticle`, `ArticleVersion`, `ArticleCategory`, `FAQData`

### Surveys and Feedback
Types for collecting customer feedback:
- `Feedback`, `Survey`, `SurveyResponse`, `SurveyQuestion`

### Omni-Channel and Routing
Types for multi-channel service routing:
- `OmniChannel`, `PresenceStatus`, `PresenceDeclineReason`
- `RoutingConfiguration`, `ServiceResource`, `WorkCapacity`

### Automation and Flow
Types for process automation:
- `Flow`, `FlowInterview`

### Authentication
Types for API access management:
- `APIKey`, `Token`

## Scalar Types

| Scalar | Description |
|--------|-------------|
| `DateTime` | ISO 8601 date-time string |
| `Date` | ISO 8601 date string |
| `ID` | Salesforce 18-character record ID |
| `JSON` | Arbitrary JSON value |
| `URL` | A valid URL string |

## Key Relationships

- A `Case` belongs to one `Contact` and one `Account`
- A `Case` may have many `CaseComment` and `CaseFeed` entries
- A `Case` may have an associated `Entitlement` and `Milestone`
- A `ChatSession` is linked to a `Visitor` and produces a `ChatTranscript`
- An `AgentWork` routes work items from a `Queue` to an `AgentDetails` record
- A `KnowledgeArticle` has multiple `ArticleVersion` records and belongs to `ArticleCategory`
- A `Survey` contains multiple `SurveyQuestion` records; responses are captured as `SurveyResponse`
- A `Flow` manages automation logic; `FlowInterview` tracks individual executions

## Usage Notes

This schema is conceptual and intended to document the Salesforce Service Cloud data model for integration planning, code generation, and developer tooling. Actual Salesforce GraphQL access is provided through the [Salesforce GraphQL API (Connect REST API)](https://developer.salesforce.com/docs/platform/graphql/guide/graphql-overview.html) using the Salesforce object query language (SOQL) projection syntax.

For production use, fields and types should be validated against your specific Salesforce org configuration, installed packages, and API version.
