FROM mcr.microsoft.com/dotnet/core/aspnet:3.1
ARG source
WORKDIR /src
EXPOSE 80
COPY ${source:-obj/Docker/publish} .
ENTRYPOINT ["dotnet", "ContainerWebApp.dll"]
