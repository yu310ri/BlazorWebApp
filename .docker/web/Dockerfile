FROM mcr.microsoft.com/dotnet/sdk AS build-env
COPY ../../wwwroot /var/wwwroot

FROM nginx:alpine
WORKDIR /var/wwwroot 
COPY --from=buid-env /var/wwwroot .
COPY .default.conf /etc/nginx/conf.d/default.conf