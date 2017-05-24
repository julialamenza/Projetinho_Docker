FROM debian
MAINTAINER Julia Lamenza <jlamenza@gmail.com>
RUN apt-get update && apt-get install -y nginx
CMD ["nginx", "-g", "daemon off;"]
EXPOSE 80 443
