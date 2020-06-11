FROM mcr.microsoft.com/dotnet/core/aspnet:2.1
WORKDIR /app
COPY samples/MusicStore/bin/Release/netcoreapp2.1/publish /app/
COPY samples/MusicStore/config.json /app/

ENV ASPNETCORE_URLS=http://0.0.0.0:8080

ENTRYPOINT ["dotnet", "MusicStore.dll"]