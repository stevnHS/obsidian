```shell
dotnet ef migrations add InitialCreate -p Persistence -s API
dotnet ef database update -p Persistence -s API
dotnet ef database drop -p Persistence -s API
```