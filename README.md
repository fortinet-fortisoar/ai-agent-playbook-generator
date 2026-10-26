# Release Information

- **Version**: 1.0.0

- **Certified**: Yes

- **Publisher**: Fortinet

- **Scope**: Playbook Designer

- **Verified with Models**: Fortinet FortiAI (AI model Medium)

# Playbook Generation Agent

A conversational agent that interprets natural-language requests and generates structured, actionable security playbooks tailored to FortiSOAR.

## Installation

This agent installs along with the FortiAI solution pack.

## Configuration

The Playbook Generation agent ships with a configuration that has access to all shipped MCP servers. For custom configuration, refer to the *Configuration* section of the [FortiAI](https://github.com/fortinet-fortisoar/solution-pack-fortinet-advisor) solution pack documentation.

> [!Note]
> Refer to [Configuring MCP Servers](https://docs.fortinet.com/document/fortisoar/8.0.0/administration-guide/823139/mcp-servers#Configure_MCP_Servers) on FortiSOAR platform documentation for information on configuring a custom MCP server.

### Prerequisites

The following prerequisites must be met before using this agent:

- The FortiAI solution pack must be installed and configured with the Fortinet FortiAI connector.

  - To configure the FortiAI solution pack, refer to the [FortiAI](https://github.com/fortinet-fortisoar/solution-pack-fortinet-advisor/) solution pack documentation.
  - To configure the Fortinet FortiAI connector, refer to the [Fortinet FortiAI](https://docs.fortinet.com/fortisoar/connectors/fortinet-fortiai) connector documentation.

> [!Note]
> The FortiAI solution pack and the Fortinet FortiAI connector are preconfigured out-of-the-box with FortiSOAR `v8.0.1` and later.

## Input Parameters

The input must be provided as a JSON object.

| Parameter              | Description                                             |
|------------------------|---------------------------------------------------------|
| `question`             | The question that needs to be answered.                 |
| `context`              | The FortiSOAR context from where the question is asked. |
| `previous_response_id` | The ID of the previous response (if applicable).        |

## Response

The output is returned as a JSON object.

| Parameter     | Description                                                                   |
|---------------|-------------------------------------------------------------------------------|
| `answer`      | The answer to the query.                                                      |
| `response_id` | The ID of the response, used as `previous_response_id` in follow-up requests. |