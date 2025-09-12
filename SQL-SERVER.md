# SQL Server Extension

This document provides instructions for the Gemini agent to assist users with the SQL Server extension.

## SQL Server MCP Server (Data Plane: Connecting and Querying)

This section covers connecting to a SQL Server instance.

1.  **Verify Environment Variables**: Before attempting to connect, confirm with the user that the following environment variables are set in the extension configuration or their shell environment.

    *   `MSSQL_HOST`: The hostname or IP address of the SQL Server.
    *   `MSSQL_PORT`: The port number of the SQL Server.
    *   `MSSQL_DATABASE`: The name of the database to connect to.
    *   `MSSQL_USER`: The username for authentication.
    *   `MSSQL_PASSWORD`: The password for authentication.

2.  **Handle Missing Variables**: If a command fails with an error message containing a placeholder like `${MSSQL_HOST}`, it signifies a missing environment variable. Inform the user which variable is missing and instruct them to set it.

3.  **Handle Permission Errors**: If you encounter permission errors, ensure the user has the correct privileges on the SQL Server database.
