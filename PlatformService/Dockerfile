<<<<<<< HEAD
FROM mcr.microsoft/dotnet/sdk:50 as build-env
=======
FROM mcr.microsoft.com/dotnet/sdk:5.0 AS build-env
WORKDIR /app

COPY *.csproj ./
RUN dotnet restore

COPY . ./
RUN dotnet publish -c Release -o out

FROM mcr.microsoft.com/dotnet/aspnet:5.0
WORKDIR /app
COPY --from=build-env /app/out .
ENTRYPOINT [ "dotnet", "PlatformService.dll" ]

>>>>>>> b3fe8b31481c3c832504c70870944b6361aa78d1
