<!--
  ~ Copyright (c) 2023-2024 Datalayer, Inc.
  ~
  ~ BSD 3-Clause License
-->

[![Datalayer](https://assets.datalayer.tech/datalayer-25.svg)](https://datalayer.io)

[![Become a Sponsor](https://img.shields.io/static/v1?label=Become%20a%20Sponsor&message=%E2%9D%A4&logo=GitHub&style=flat&color=1ABC9C)](https://github.com/sponsors/datalayer)

# 🦜 🔗 Langchain MCP Client

[![Github Actions Status](https://github.com/datalayer/langchain-mcp-client/workflows/Build/badge.svg)](https://github.com/datalayer/langchain-mcp-client/actions/workflows/build.yml)
[![PyPI - Version](https://img.shields.io/pypi/v/langchain-mcp-client)](https://pypi.org/project/langchain-mcp-client)

This simple [Model Context Protocol (MCP)](https://modelcontextprotocol.io/)
client demonstrates the use of MCP server tools by LangChain ReAct Agent.

It leverages a utility function `convert_mcp_to_langchain_tools()` from
[`langchain_mcp_tools`](https://pypi.org/project/langchain-mcp-tools/).  
This function handles parallel initialization of specified multiple MCP servers
and converts their available tools into a list of LangChain-compatible tools
([List[BaseTool]](https://python.langchain.com/api_reference/core/tools/langchain_core.tools.base.BaseTool.html#langchain_core.tools.base.BaseTool)).

This is an adpated version of: https://github.com/hideya/mcp-client-langchain-py.

## Usage

```bash
python langchain_mcp_client/cli_chat.py
```

`.env` file is required with the all the necessary `API_KEYS`.

Models to invoke and MCP servers to use can be configured in `llm_mcp_config.json5`.

At the prompt, you can simply press Enter to use example queries that perform MCP server tool invocations.-
Example queries can also be configured in  `llm_mcp_config.json5`.