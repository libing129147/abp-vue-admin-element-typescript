FROM mcr.microsoft.com/dotnet/core/sdk:3.1 AS runtime
LABEL maintainer="colin.in@foxmail.com"
WORKDIR /app

COPY . /app

ENV TZ=Asia/Shanghai
RUN ln -snf /usr/share/zoneinfo/$TZ /etc/localtime && echo '$TZ' > /etc/timezone

EXPOSE 80/tcp
VOLUME [ "./app/Logs" ]

ENTRYPOINT ["dotnet", "LINGYUN.Abp.MessageService.HttpApi.Host.dll"]