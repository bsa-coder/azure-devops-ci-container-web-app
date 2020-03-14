FROM mcr.microsoft.com/dotnet/core/aspnet:3.1
ARG source
WORKDIR /src
EXPOSE 80
COPY obj/Docker/publish /app
ENTRYPOINT ["dotnet", "ContainerWebApp.dll"]
