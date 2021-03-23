#See https://aka.ms/containerfastmode to understand how Visual Studio uses this Dockerfile to build your images for faster debugging.

FROM mcr.microsoft.com/dotnet/core/aspnet:3.1-buster-slim AS base
WORKDIR /app
EXPOSE 80

FROM mcr.microsoft.com/dotnet/core/sdk:3.1-buster AS build
WORKDIR /src
COPY ["WebAppInDocker.Api/WebAppInDocker.Api.csproj", "WebAppInDocker.Api/"]
RUN dotnet restore "WebAppInDocker.Api/WebAppInDocker.Api.csproj"
COPY . .
WORKDIR "/src/WebAppInDocker.Api"
RUN dotnet build "WebAppInDocker.Api.csproj" -c Release -o /app/build

FROM build AS publish
RUN dotnet publish "WebAppInDocker.Api.csproj" -c Release -o /app/publish

FROM base AS final
WORKDIR /app
COPY --from=publish /app/publish .
ENTRYPOINT ["dotnet", "WebAppInDocker.Api.dll"]