# Use the latest image of Ubuntu
FROM mcr.microsoft.com/powershell:lts-ubuntu-22.04

# Install curl and gnupg2
RUN apt-get update && apt-get install -y curl gnupg2

# Install Azure CLI
# RUN curl -sL https://aka.ms/InstallAzureCLIDeb | bash

# Install AZ Modules
USER root
RUN /usr/bin/pwsh -Command "Install-Module -Name ALZ -Force -Scope AllUsers"

# Clean up
RUN apt-get clean && rm -rf /var/lib/apt/lists/*

