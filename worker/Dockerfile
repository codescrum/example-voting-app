FROM microsoft/dotnet:1.0.0-preview1
MAINTAINER Cristian Riaño <cristian.riano@codescrum.com>

WORKDIR /app

ADD src/ /app/src/

RUN dotnet restore -v minimal src/ \
    && dotnet publish -c Release -o ./ src/Worker/ \
    && rm -rf src/ $HOME/.nuget/

CMD dotnet Worker.dll
