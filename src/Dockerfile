FROM mcr.microsoft.com/dotnet/runtime:5.0
WORKDIR /app

# Copy the published web app
COPY /src/ /app

# Run command
ENTRYPOINT ["dotnet", "DevOpsChallenge.SalesApi.dll"]
