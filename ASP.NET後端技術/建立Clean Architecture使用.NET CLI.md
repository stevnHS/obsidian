#dotnet-cli #clean-architecure #dotnet9

## 新增方案與專案
```sh
dotnet new sln

dotnet new webapi -n API -controllers    #startup project
dotnet new classlib -n Domain
dotnet new classlib -n Application
dotnet new classlib -n Persistence

dotnet sln add API
dotnet sln add Domain
dotnet sln add Application
dotnet sln add Persistence
```
## 新增專案參考(Project Reference)
```sh
dotnet add API/API.csproj reference Application/Application.csproj

dotnet add Application/Application.csproj reference Domain/Domain.csproj Persistence/Persistence.csproj

dotnet add Persistence/Persistence.csproj reference Domain/Domain.csproj
```
## 準備.gitignore檔案
```sh
dotnet new gitignore
```
已經包含很完整的清單(obj/,bin/,node_modules...)，可能還會加入sqlite或API/appsettings.json

## 啟動專案
```shell
dotnet run --project API 
dotnet watch --project API
dotnet dev-certs https --trust #self signed certificates
```