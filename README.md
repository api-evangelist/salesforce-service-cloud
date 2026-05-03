# Salesforce Service Cloud

Salesforce Service Cloud is a customer service and support platform that helps businesses deliver smarter, faster, and more personalized customer service across all channels.

**URL:** https://www.salesforce.com/service-cloud/

**Tags:** Case Management, CRM, Customer Service, Help Desk, Support, Ticketing

## APIs

### Salesforce Service Cloud REST API
- **OpenAPI:** [salesforce-service-cloud-rest-openapi.yml](openapi/salesforce-service-cloud-rest-openapi.yml)
- **Documentation:** https://developer.salesforce.com/docs/atlas.en-us.api_rest.meta/api_rest/

### Live Agent REST API
- **OpenAPI:** [salesforce-live-agent-openapi.yml](openapi/salesforce-live-agent-openapi.yml)
- **Documentation:** https://developer.salesforce.com/docs/atlas.en-us.live_agent_rest.meta/live_agent_rest/

### Service Cloud Streaming API
- **AsyncAPI:** [salesforce-streaming-api-asyncapi.yml](asyncapi/salesforce-streaming-api-asyncapi.yml)
- **Documentation:** https://developer.salesforce.com/docs/atlas.en-us.api_streaming.meta/api_streaming/

### Knowledge API
- **Documentation:** https://developer.salesforce.com/docs/atlas.en-us.knowledge_dev.meta/knowledge_dev/

### Einstein Bot API
- **Documentation:** https://developer.salesforce.com/docs/atlas.en-us.bot_cookbook.meta/bot_cookbook/

### Agentforce Service Agent API
- **Documentation:** https://developer.salesforce.com/docs/einstein/genai/guide/get-started-agents.html

## Common Resources

| Type | URL |
|------|-----|
| Getting Started | https://developer.salesforce.com/docs/atlas.en-us.api_rest.meta/api_rest/quickstart.htm |
| Authentication | https://help.salesforce.com/articleView?id=sf.remoteaccess_authenticate.htm |
| Rate Limits | https://developer.salesforce.com/docs/atlas.en-us.salesforce_app_limits_cheatsheet.meta/salesforce_app_limits_cheatsheet/ |
| Developer Portal | https://developer.salesforce.com/ |
| Trailhead Learning | https://trailhead.salesforce.com/ |
| API Status | https://status.salesforce.com/ |
| Support | https://help.salesforce.com/ |
| Community | https://trailblazercommunity.salesforce.com/ |
| Pricing | https://www.salesforce.com/service-cloud/pricing/ |
| Terms of Service | https://www.salesforce.com/company/legal/agreements/ |
| Privacy Policy | https://www.salesforce.com/company/privacy/ |
| GitHub Organization | https://github.com/developerforce |

## Artifacts

### OpenAPI Specifications

| Spec | Description |
|------|-------------|
| [salesforce-service-cloud-rest-openapi.yml](openapi/salesforce-service-cloud-rest-openapi.yml) | Service Cloud REST API — cases, contacts, accounts, knowledge |
| [salesforce-live-agent-openapi.yml](openapi/salesforce-live-agent-openapi.yml) | Live Agent REST API — chat session management |

### AsyncAPI Specifications

| Spec | Description |
|------|-------------|
| [salesforce-streaming-api-asyncapi.yml](asyncapi/salesforce-streaming-api-asyncapi.yml) | Streaming API — real-time event subscriptions |

### Spectral Rules

| Ruleset | Description |
|---------|-------------|
| [salesforce-service-cloud-rules.yml](rules/salesforce-service-cloud-rules.yml) | Spectral rules enforcing Service Cloud API conventions |

### Capabilities

| Capability | Description |
|------------|-------------|
| [case-management.yaml](capabilities/case-management.yaml) | Case management workflow — cases, contacts, live chat (12 tools) |

**Shared Definitions:**

| Shared | Description |
|--------|-------------|
| [service-cloud-rest-api.yaml](capabilities/shared/service-cloud-rest-api.yaml) | Service Cloud REST API consumed definition |
| [live-agent-api.yaml](capabilities/shared/live-agent-api.yaml) | Live Agent API consumed definition |

### JSON Schemas

| Schema | Description |
|--------|-------------|
| [salesforce-case-schema.json](json-schema/salesforce-case-schema.json) | Case record schema |

### JSON Structures

| Structure | Description |
|-----------|-------------|
| [salesforce-service-cloud-case-structure.json](json-structure/salesforce-service-cloud-case-structure.json) | Case sObject field documentation |

### JSON-LD Context

| Context | Description |
|---------|-------------|
| [salesforce-service-cloud-context.jsonld](json-ld/salesforce-service-cloud-context.jsonld) | JSON-LD context for Salesforce Service Cloud entities |

### Examples

| Example | Description |
|---------|-------------|
| [salesforce-service-cloud-create-case-example.json](examples/salesforce-service-cloud-create-case-example.json) | Create Case request/response |
| [salesforce-service-cloud-query-cases-example.json](examples/salesforce-service-cloud-query-cases-example.json) | SOQL query for open high-priority cases |

### Vocabulary

| Vocabulary | Description |
|------------|-------------|
| [salesforce-service-cloud-vocabulary.yml](vocabulary/salesforce-service-cloud-vocabulary.yml) | Salesforce Service Cloud domain vocabulary |

## Maintainers

- Kin Lane (kin@apievangelist.com)
