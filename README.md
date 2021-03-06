# dotnet-dbinfo

[![NuGet][main-nuget-badge]][main-nuget]

[main-nuget]: https://www.nuget.org/packages/dotnet-dbinfo/
[main-nuget-badge]: https://img.shields.io/nuget/v/dotnet-dbinfo.svg?style=flat-square&label=nuget

A simple cross-platform command-line tool for get useful database information (in json format).

## Get started

Download the .NET Core SDK [2.1.300](https://aka.ms/DotNetCore21) or newer.
Once installed, run this command:

```
dotnet tool install -g dotnet-dbinfo
```

Or update to the latest version:
```
dotnet tool update -g dotnet-dbinfo
```

## Usage

### Microsoft SQL Server

```
Usage: dotnet dbinfo sqlserver server database user password

Arguments:

  server                    Name of the database server

  database                  Name of the database instance

  user                      Login name of the user

  password                  Password of the user        
```

Example:
```
dotnet dbinfo sqlserver .\SQLEXPRESS master sa Pass1234
```

### Azure SQL

```
Usage: dotnet dbinfo sqlazure server database user password

Arguments:

  server                    Name of the database server

  database                  Name of the database instance

  user                      Login name of the user

  password                  Password of the user        
```

Example:
```
dotnet dbinfo sqlazure .\SQLEXPRESS master sa Pass1234
```


### AWS DynamoDb

```
Usage: dotnet dbinfo dynamodb regionendpoint [accesskey] [secretkey]

Arguments:

  regionendpoint            Region (for example: us-east-1)

  accesskey/secretkey       (OPTIONAL) If not set, tool uses AWS credentials profile file on your local system         
  
```

Example:
```
dotnet dbinfo dynamodb us-east-1
```

### Azure CosmosDb

```
Usage: dotnet dbinfo cosmosdb endpointUri primaryKey database

Arguments:

  endpointUri            Your endpoint URL from the Portal

  primaryKey             Your primary key   

  database               Name of the database    
  
```

Example:
```
dotnet dbinfo cosmosdb https://test.documents.azure.com:443/ Y7Tr6jZy10Jh6FOo4hCP4LR128ekLOczs4a5fQlEjH0TehgWfOdilWp2GvyQ1pmDxP3zQFXF11CclKgsg9vMz4Q== ToDoList
```

### MongoDb

```
Usage: dotnet dbinfo mongodb host:port database user password

Arguments:

  host:port             Host and port of the MongoDb server

  database              Name of the database 

  user                  Login name of the user

  password              Password of the user   
  
```

Example:
```
dotnet dbinfo mongodb localhost:27017 my_database my_user password123
```

> **Hint:** The **user** must have the necessary **permissions** for the database!

