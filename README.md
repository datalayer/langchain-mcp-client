<!--
  ~ Copyright (c) 2023-2024 Datalayer, Inc.
  ~
  ~ BSD 3-Clause License
-->

[![Datalayer](https://assets.datalayer.tech/datalayer-25.svg)](https://datalayer.io)

[![Become a Sponsor](https://img.shields.io/static/v1?label=Become%20a%20Sponsor&message=%E2%9D%A4&logo=GitHub&style=flat&color=1ABC9C)](https://github.com/sponsors/datalayer)

# 🦜 🔗 LangChain MCP Client

[![Github Actions Status](https://github.com/datalayer/langchain-mcp-client/workflows/Build/badge.svg)](https://github.com/datalayer/langchain-mcp-client/actions/workflows/build.yml)
[![PyPI - Version](https://img.shields.io/pypi/v/langchain-mcp-client)](https://pypi.org/project/langchain-mcp-client)

This simple [Model Context Protocol (MCP)](https://modelcontextprotocol.io/)
client demonstrates the use of MCP server tools by LangChain ReAct Agent.
- 🌐 Seamlessly connect to any MCP servers.
- 🤖 Use any LangChain-compatible LLM for flexible model selection.
- 💬 Interact via CLI, enabling dynamic conversations.

## Conversion to LangChain Tools

It leverages a utility function `convert_mcp_to_langchain_tools()` from
[`langchain_mcp_tools`](https://pypi.org/project/langchain-mcp-tools/).  
This function handles parallel initialization of specified multiple MCP servers
and converts their available tools into a list of LangChain-compatible tools
([List[BaseTool]](https://python.langchain.com/api_reference/core/tools/langchain_core.tools.base.BaseTool.html#langchain_core.tools.base.BaseTool)).

## Installation

The python version should be 3.11 or higher.

```bash
pip install langchain_mcp_client
```

## Configuration

Create a `.env` file containing all the necessary `API_KEYS` to access your LLM.

Configure the LLM, MCP servers, and prompt example in the `llm_mcp_config.json5` file:

1. **LLM Configuration**: Set up your LLM parameters.
2. **MCP Servers**: Specify the MCP servers to connect to.
3. **Example Queries**: Define example queries that invoke MCP server tools. Press Enter to use these example queries when prompted.

## Usage

```bash
langchain-mcp-client
```

Below an example with [jupyter-mcp-server](https://github.com/datalayer/jupyter-mcp-server):

![](https://assets.datalayer.tech/jupyter-mcp/jupyter-mcp-server-cli.gif)

## Credits

This initial code of this repo is taken from  from [hideya/mcp-client-langchain-py](https://github.com/hideya/mcp-client-langchain-py) (MIT License).