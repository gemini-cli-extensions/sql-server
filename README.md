# Gemini CLI Extension - SQL Server

> [!NOTE]
> This extension is currently in beta (pre-v1.0), and may see breaking changes until the first stable release (v1.0).

This Gemini CLI extension provides a set of tools to interact with [Microsoft SQL Server](https://docs.microsoft.com/en-us/sql/) instances. It allows you to manage your databases, execute queries, and explore schemas directly from the [Gemini CLI](https://google-gemini.github.io/gemini-cli/), using natural language prompts.

Learn more about [Gemini CLI Extensions](https://github.com/google-gemini/gemini-cli/blob/main/docs/extensions/index.md).
> [!IMPORTANT]
> **We Want Your Feedback!**
> Please share your thoughts with us by filling out our feedback [form][form]. 
> Your input is invaluable and helps us improve the project for everyone.

[form]: https://docs.google.com/forms/d/e/1FAIpQLSfEGmLR46iipyNTgwTmIDJqzkAwDPXxbocpXpUbHXydiN1RTw/viewform?usp=pp_url&entry.157487=sql-server

## Why Use the SQL Server Extension?

* **Natural Language Management:** Stop wrestling with complex commands. Explore schemas and query data by describing what you want in plain English.
* **Seamless Workflow:** As a Google-developed extension, it integrates seamlessly into the Gemini CLI environment. No need to constantly switch contexts for common database tasks.
* **Code Generation:** Accelerate development by asking Gemini to generate data classes and other code snippets based on your table schemas.


## Prerequisites

Before you begin, ensure you have the following:

* One of the supported agent harnesses, installed and authenticated:
  * [Gemini CLI](https://github.com/google-gemini/gemini-cli) (v0.6.0+)
  * [Claude Code](https://code.claude.com)
  * [Codex](https://developers.openai.com/codex)
  * [Antigravity CLI](https://antigravity.google)
* [Node.js](https://nodejs.org/) (the MCP server runs via `npx`).
* A running SQL Server instance.
* A user with database-level permissions to execute queries.

## Getting Started

### Installation

All harnesses use the same plugin; the MCP server runs via `npx` (no binary to download). Install with your harness of choice:

**Gemini CLI**

```bash
gemini extensions install https://github.com/gemini-cli-extensions/sql-server
```

**Claude Code**

```bash
claude plugin marketplace add gemini-cli-extensions/sql-server
claude plugin install sql-server@sql-server
```

**Codex**

```bash
codex plugin marketplace add gemini-cli-extensions/sql-server
codex plugin add sql-server@sql-server
```

**Antigravity**

```bash
agy plugin install https://github.com/gemini-cli-extensions/sql-server
```

See [Configuration](#configuration) for how each harness supplies the connection settings.

### Configuration

The plugin connects to SQL Server using these settings:

*   `MSSQL_HOST`: (Optional) The SQL Server host. Defaults to `localhost`.
*   `MSSQL_PORT`: (Optional) The SQL Server port. Defaults to `1433`.
*   `MSSQL_DATABASE`: The name of the database to connect to.
*   `MSSQL_USER`: The database username.
*   `MSSQL_PASSWORD`: The password for the database user.

How you supply them depends on the harness:

*   **Gemini CLI**: prompted on install and saved to the extension's `.env`. View or update later with `gemini extensions list` / `gemini extensions config sql-server [setting] [--scope user|workspace]` (restart the CLI to apply).
*   **Claude Code**: pass `--config KEY=VALUE` on install (repeatable), or run `/plugin` inside Claude Code.
*   **Codex** and **Antigravity**: export the variables in your shell before starting:

#### PowerShell
```powershell
$env:MSSQL_HOST = '<your-sql-server-host>'  # Optional: defaults to localhost
$env:MSSQL_PORT = '<your-sql-server-port>'  # Optional: defaults to 1433
$env:MSSQL_DATABASE = '<your-database-name>'
$env:MSSQL_USER = '<your-database-user>'
$env:MSSQL_PASSWORD = '<your-database-password>'
```

#### Bash
```bash
export MSSQL_HOST="<your-sql-server-host>"  # Optional: defaults to localhost
export MSSQL_PORT="<your-sql-server-port>"  # Optional: defaults to 1433
export MSSQL_DATABASE="<your-database-name>"
export MSSQL_USER="<your-database-user>"
export MSSQL_PASSWORD="<your-database-password>"
```

> [!NOTE]
> See [Troubleshooting](#troubleshooting) for debugging your configuration.

### Start Gemini CLI

To start the Gemini CLI, use the following command:

```bash
gemini
```

> [!WARNING]
> **Changing Instance & Database Connections**
> Currently, the database connection must be configured before starting the Gemini CLI and can not be changed during a session.
> To save and resume conversation history use command: `/chat save <tag>` and `/chat resume <tag>`.

## Usage Examples

Interact with SQl Server using natural language right from your IDE:

* **Explore Schemas and Data:**
  * "Show me all tables in the 'orders' database."
  * "What are the columns in the 'products' table?"
  * "How many orders were placed in the last 30 days, and what were the top 5 most purchased items?"
* **Generate Code:**
  * "Generate a Python dataclass to represent the 'customers' table."

## Supported Tools

* `list_tables`: lists schema information for all or specified tables in a SQL server database.
* `execute_sql`: executes a SQL statement against a SQL Server database.

## Additional Extensions

Find additional extensions to support your entire software development lifecycle at [github.com/gemini-cli-extensions](https://github.com/gemini-cli-extensions), including:
* [Cloud SQL for SQL Server extension](https://github.com/gemini-cli-extensions/cloud-sql-sqlserver)
* and more!

## Troubleshooting

Use `gemini --debug` to enable debugging.

Common issues:

* "✖ Error during discovery for server: MCP error -32000: Connection closed": The database connection has not been established. Ensure your configuration is set via environment variables.
* "✖ MCP ERROR: Error: spawn npx ENOENT": Node.js/`npx` is not installed or not on your `PATH`. Install Node.js (which provides `npx`).
* "npm error"/network failures on first run: `npx` fetches `@toolbox-sdk/server` on first launch, so it needs network access. Retry once connectivity is available.
