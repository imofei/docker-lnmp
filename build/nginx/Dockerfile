FROM nginx:1.19.5
MAINTAINER mofei <root@mofei.org>

# Change Timezone
ARG TIME_ZONE=UTC
ENV TIME_ZONE ${TIME_ZONE}
RUN ln -snf /usr/share/zoneinfo/$TIME_ZONE /etc/localtime && echo $TIME_ZONE > /etc/timezone

# Change Webroot Permissions
RUN mkdir /etc/nginx/html
RUN chown -R www-data.www-data /etc/nginx/html/ /var/log/nginx/