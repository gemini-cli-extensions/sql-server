This Gemini CLI extension provides a set of tools to interact with [Microsoft SQL Server](https://docs.microsoft.com/en-us/sql/) instances. It allows you to manage your databases, execute queries, and explore schemas directly from the [Gemini CLI](https://google-gemini.github.io/gemini-cli/), using natural language prompts.

## Why Use the SQL Server Extension?

* **Natural Language Management:** Stop wrestling with complex commands. Explore schemas and query data by describing what you want in plain English.
* **Seamless Workflow:** As a Google-developed extension, it integrates seamlessly into the Gemini CLI environment. No need to constantly switch contexts for common database tasks.
* **Code Generation:** Accelerate development by asking Gemini to generate data classes and other code snippets based on your table schemas.

## Prerequisites

Before you begin, ensure you have the following:

* [Gemini CLI](https://github.com/google-gemini/gemini-cli) installed.
* A running SQL Server instance.
* A user with database-level permissions to execute queries.

## Installation

To install the extension, use the command:

```bash
gemini extensions install github.com/gemini-cli-extensions/sql-server
```

## Configuration

Set the following environment variables before starting the Gemini CLI:

* `MSSQL_HOST`: The hostname or IP address of the SQL Server.
* `MSSQL_PORT`: The port number of the SQL Server.
* `MSSQL_DATABASE`: The name of the database to connect to.
* `MSSQL_USER`: The username for authentication.
* `MSSQL_PASSWORD`: The password for authentication.

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

Find additional extensions to support your entire software development lifecycle at [github.com/gemini-cli-extensions](https://github.com/gemini-cli-extensions).

## Troubleshooting

* "cannot execute binary file": Ensure the correct binary for your OS/Architecture has been downloaded. See [Installing the server](https://googleapis.github.io/genai-toolbox/getting-started/introduction/#installing-the-server) for more information.
