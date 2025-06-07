# escape=`
FROM mcr.microsoft.com/windows/servercore:ltsc2022

SHELL ["powershell", "-Command", "$ErrorActionPreference = 'Stop';"]

RUN Invoke-WebRequest -Uri https://github.com/prometheus-community/windows_exporter/releases/download/v0.30.6/windows_exporter-0.30.6-amd64.exe -OutFile C:\\windows_exporter.exe

EXPOSE 9182

ENTRYPOINT ["C:\\windows_exporter.exe"]