ARG ELK_VERSION

# https://github.com/elastic/logstash-docker
FROM docker.elastic.co/logstash/logstash-oss:${ELK_VERSION}

#CMD ['-f', '/usr/share/logstash/pipeline/logstash.conf']

# Add your logstash plugins setup here
# Example: RUN logstash-plugin install logstash-filter-json

RUN rm -f /usr/share/logstash/pipeline/logstash.conf

ADD config/ /usr/share/logstash/config/
ADD pipeline/ /usr/share/logstash/pipeline/
ADD patterns/ /usr/share/logstash/patterns/
