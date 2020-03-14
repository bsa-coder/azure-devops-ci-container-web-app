FROM mcr.microsoft.com/dotnet/core/sdk:3.1 AS build-env
WORKDIR /src

# Copy csproj and restore as distinct layers
RUN dotnet restore

# Copy everything else and build
RUN dotnet publish -c Release -o out

# Build runtime image
FROM mcr.microsoft.com/dotnet/core/aspnet:3.1
ENTRYPOINT ["dotnet", "ContainerWebApp.dll"]