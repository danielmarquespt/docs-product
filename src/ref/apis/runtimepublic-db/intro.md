---
summary: Provides functionality to allow you to integrate with your external databases.
tags: >-
  support-application_development; support-Database;
  support-Integrations_Extensions
---

# RuntimePublic.Db API

The RuntimePublic.Db API provides functionality to allow you to integrate with your external databases.

With this API you enable your extension modules to call the databases configured in the environment management console. It is, by default, imported to your extension project when you create it in Integration Studio. To use this API you only need to reference its classes in your extension's project.

It is available under the `OutSystems.RuntimePublic.Db` .NET namespace.

## Classes

| Name | Description |
| :--- | :--- |
| [Command](intro.md#command) | Represents a command to execute queries. |
| [CommittableTransaction](intro.md#committabletransaction) | Represents a transaction that needs to be explicitly managed using commit and roll back operations. Can be used for selecting, inserting, updating, and deleting data. |
| [Connection](intro.md#connection) | Represents a connection to a database. |
| [DatabaseAccess](intro.md#databaseaccess) | Creates DatabaseProvider instances to access a database. |
| [DatabaseProvider](intro.md#databaseprovider) | Provides access to a specific database. |
| [DataParameter](intro.md#dataparameter) | Represents the query parameters associated with a command. |
| [RequestTransaction](intro.md#requesttransaction) | Represents the transaction that is automatically managed by the platform. The transaction starts at the beginning of the web request, and is committed when the response is sent to the client. Can be used for selecting, inserting, updating, and deleting data. |
| [SqlHelper](intro.md#sqlhelper) | Functions to assist on the manipulation of SQL statements members. |

## Using the API

* [Call a Stored Procedure](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/ref/apis/runtimepublic-db/call-a-stored-procedure.md%3E)
* [Insert Data in the Application Database](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/ref/apis/runtimepublic-db/insert-data-in-the-application-database.md%3E)
* [Query Data from an External Database](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/ref/apis/runtimepublic-db/query-data-from-an-external-database.md%3E)

## API Reference

### Command

Represents a command to execute queries.

#### Methods

| Name | Description |  |
| :--- | :--- | :--- |
| [DataParameter](intro.md#dataparameter) CreateParameter\(string name, DbType type, object value\) | Adds a parameter to the command with a given type and value. The parameter value is modified to a compatible database value. |  |
| [DataParameter](intro.md#dataparameter) CreateParameter\(string name\) | Adds a parameter to the command. The parameter value is modified to a compatible database value. void Dispose\(\) | Frees the resources used by this object. |
| int ExecuteNonQuery\(\) | Executes the command and returns the number of rows affected. |  |
| IDataReader ExecuteReader\(\) | Executes the command text returning the resulting System.Data.IDataReader. |  |
| object ExecuteScalar\(\) | Executes the query, and returns the first column of the first row in the resultset returned by the query. Extra columns or rows are ignored. |  |
| [Connection](intro.md#connection) GetConnection\(\) | Returns the database connection associated to this command. |  |
| IDbCommand GetDriverCommand\(\) | Returns the native command object used by the stack in which the application is running. |  |
| [DataParameter](intro.md#dataparameter) GetParameter\(string columnName\) | Gets the parameter with the specified name. |  |

#### Members

| Name | Description |
| :--- | :--- |
| string CommandText | Gets or sets the SQL statements to execute. |
| int CommandTimeout | Gets or sets the command execution timeout. |

### CommittableTransaction

Represents a transaction that needs to be explicitly managed using commit and roll back operations. Can be used for selecting, inserting, updating, and deleting data.

#### Methods

| Name | Description |
| :--- | :--- |
| void Close\(\) | Rolls back a transaction from a pending state and closes the transaction. |
| void Commit\(\) | Commits the transaction. |
| [Command](intro.md#command) CreateCommand\(string sql\) | Creates a command to be executed in this transaction. |
| [Command](intro.md#command) CreateCommand\(\) | Creates an empty command to be executed in this transaction. |
| void Dispose\(\) | Releases the transaction and frees the resources used by this object. |
| [Connection](intro.md#connection) GetConnection\(\) | Gets the database connection associated with this transaction. |
| IDbTransaction GetDriverTransaction\(\) | Returns the native transaction object used by the stack in which the application is running. It allows to reuse existing code that receives a native transaction object as parameter. |
| void Rollback\(\) | Rolls back a transaction from a pending state. |

### Connection

Represents a connection to a database.

#### Methods

| Name | Description |
| :--- | :--- |
| [CommittableTransaction](intro.md#committabletransaction) BeginReadUncommittedTransaction\(\) | Creates an [OutSystems.RuntimePublic.Db.CommittableTransaction](intro.md#committabletransaction) with the transaction isolation level set to read uncommitted.%%**Warning: This method has been deprecated.** |
| [CommittableTransaction](intro.md#committabletransaction) BeginTransaction\(\) | Creates an [OutSystems.RuntimePublic.Db.CommittableTransaction](intro.md#committabletransaction) with the transaction isolation level set to read committed.%%**Warning: This method has been deprecated.** |
| void Close\(\) | Closes the connection to the database. |
| [Command](intro.md#command) CreateCommand\(string sql\) | Creates a command that does not have an associated transaction. |
| [Command](intro.md#command) CreateCommand\(\) | Creates an empty command that does not have an associated transaction. |
| void Dispose\(\) | Closes the connection and frees the resources used by this object. |
| IDbConnection GetDriverConnection\(\) | Returns the native connection object used by the stack in which the application is running. It allows to reuse existing code that receives a native connection object as parameter. |
| bool IsClosed\(\) | Checks if the connection is closed. |

### DatabaseAccess

Creates DatabaseProvider instances to access a database.

#### Methods

| Name | Description |
| :--- | :--- |
| [DatabaseProvider](intro.md#databaseprovider) ForDatabase\(string databaseName\) | Returns a database provider for a given database catalog or schema. Use it to access data managed by applications that are configured to use this database. |
| [DatabaseProvider](intro.md#databaseprovider) ForExternalDatabase\(string connectionName\) | Returns a database provider for a specific external database connection. Use it to access data managed by external systems. |
| [DatabaseProvider](intro.md#databaseprovider) ForRunningApplication\(\) | Returns a database provider to access the database of the currently running application. Use it to access data managed by the currently running application, or other applications sharing the same database. |
| [DatabaseProvider](intro.md#databaseprovider) ForSystemDatabase\(\) | Returns a database provider to access the system database. Use it to query the platform metamodel. |

### DatabaseProvider

Provides access to a specific database.

#### Methods

| Name | Description |
| :--- | :--- |
| [CommittableTransaction](intro.md#committabletransaction) GetCommitableTransaction\(\) | Returns a new transaction that needs to be managed explicitly using a commit or roll back. |
| [RequestTransaction](intro.md#requesttransaction) GetRequestTransaction\(\) | Returns the transaction that starts at the beginning of the web request and is committed when the response is sent to the client. This transaction cannot be committed or rolled back inside extensions. |

#### Members

| Name | Description |
| :--- | :--- |
| [SqlHelper](intro.md#sqlhelper) SqlHelper | Returns a [SqlHelper](intro.md#sqlhelper) instance targeted at the manipulation of SQL statements members. |
| int CommandTimeout | Gets or sets the command execution timeout. |

### DataParameter

Represents the query parameters associated with a command.

#### Methods

| Name | Description |
| :--- | :--- |
| IDbDataParameter %%GetDriverParameter\(\) | Returns the native parameter object used by the stack in which the application is running. |

#### Members

| Name | Description |
| :--- | :--- |
| DbType DbType | Gets or sets the database type. |
| int Size | Sets the size of the parameter. |
| object Value | Gets or sets the parameter value. |

### RequestTransaction

Represents the transaction that is automatically managed by the platform. The transaction starts at the beginning of the web request, and is committed when the response is sent to the client. Can be used for selecting, inserting, updating, and deleting data.

#### Methods

| Name | Description |
| :--- | :--- |
| [Command](intro.md#command) CreateCommand\(string sql\) | Creates a command to be executed in this transaction. |
| [Command](intro.md#command) CreateCommand\(\) | Creates an empty command to be executed in this transaction. |
| void Dispose\(\) | Releases the transaction and frees the resources used by this object. |
| [Connection](intro.md#connection) GetConnection\(\) | Gets the database connection associated with this transaction. |
| IDbTransaction GetDriverTransaction\(\) | Returns the native transaction object used by the stack in which the application is running. It allows to reuse existing code that receives a native data object as parameter. |
| void Release\(\) | Checks if the transaction exists, and frees the resources associated with it. Since this transaction is automatically managed by the platform, no commit or rollback operations are performed when releasing the transaction. |

### SqlHelper

Functions to assist in the manipulation of SQL statements members.

#### Methods

| Name | Description |
| :--- | :--- |
| string EscapeIdentifier\(string identifier\) | Escapes an identifier so it can be used in a query. |
| string PrefixParam\(string paramName\) | Prefixes a parameter name in order to be used as a placeholder in a query or to be used as the defacto parameter name when creating command parameters. |

