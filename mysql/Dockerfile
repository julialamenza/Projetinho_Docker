FROM debian
MAINTAINER Julia Lamenza <jlamenza@gmail.com>
RUN groupadd -r mysql && useradd -r -g mysql mysql
RUN apt-get update && DEBIAN_FRONTEND=noninteractive apt-get install -y mysql-server
EXPOSE 3306
CMD ["mysqld"]
