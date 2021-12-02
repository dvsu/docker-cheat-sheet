# Microsoft SQL Server

## Linux

### Pull docker image

```none
docker pull mcr.microsoft.com/mssql/server:2017-latest
```

or

```none
docker pull mcr.microsoft.com/mssql/server:2019-latest
```

for Microsoft SQL Server 2019.

### Start Microsoft SQL Server instance

```none
docker run -d --name mssqlserver -e "ACCEPT_EULA=Y" -e "SA_PASSWORD=5uperP@55w0rd" -p 1433:1433 -d mcr.microsoft.com/mssql/server:2017-latest
```

### Reference

- [Official Microsoft SQL Server container image](https://hub.docker.com/_/microsoft-mssql-server)
