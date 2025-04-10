# Model Context Protocol (MCP) Website Fetcher

A Model Context Protocol (MCP) server implementation that provides a simple website fetching service. This server exposes a tool that allows clients to fetch and retrieve the content of any website through the MCP protocol.

## What is MCP?

[Model Context Protocol (MCP)](https://modelcontextprotocol.io/introduction) is a protocol that enables LLMs to interact with external tools and resources. MCP servers can provide three main types of capabilities:

1. **Resources**: File-like data that can be read by clients (like API responses or file contents)
2. **Tools**: Functions that can be called by the LLM (with user approval)
3. **Prompts**: Pre-written templates that help users accomplish specific tasks

This implementation focuses on providing a tool capability for website fetching.

## Local Development

1. Clone the repository:
   ```bash
   git clone <your-repository-url>
   cd <repository-name>
   ```

2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

3. Run the MCP server:
   ```bash
   python app.py --port 8000
   ```

The server will start and listen for MCP connections on the specified port (default: 8000).

## Docker

### Local Docker Build

1. Build the Docker image:
   ```bash
   docker build -t mcp-website-fetcher .
   ```

2. Run the container:
   ```bash
   docker run -p 8000:8000 mcp-website-fetcher
   ```

### Using GitHub Container Registry

The application is automatically built and pushed to GitHub Container Registry (GHCR) on every push to the main branch. You can pull and run the latest image using:

```bash
docker pull ghcr.io/<your-github-username>/<repository-name>:main
docker run -p 8000:8000 ghcr.io/<your-github-username>/<repository-name>:main
```
