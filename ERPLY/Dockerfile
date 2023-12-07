FROM httpd:latest

# Update and install necessary packages
RUN yum update -y && \
    yum install -y zip curl && \
    yum clean all

WORKDIR /var/www/html

RUN curl -o /var/www/html/master.zip -L https://codeload.github.com/sujoyduttajad/Landing-Page-React/zip/master && \
    unzip master.zip && \
    mv Landing-Page-React-master/* . && \
    rm -rf Landing-Page-React-master.zip


EXPOSE 80

CMD ["/usr/sbin/httpd", "-D", "FOREGROUND"]
