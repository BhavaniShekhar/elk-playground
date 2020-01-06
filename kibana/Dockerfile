FROM java:8-jre

LABEL AUTHOR BHAVANISHEKHAR
ENV KIBANA_HOME /opt/kibana
ENV KIBANA_ES_URL http://localhost:9200

# Download Kibana
RUN wget -O - https://artifacts.elastic.co/downloads/kibana/kibana-7.2.0-linux-x86_64.tar.gz | tar xvz -C /opt && \
  mv /opt/ibana-7.2.0-linux-x86_64 ${KIBANA_HOME}

WORKDIR ${KIBANA_HOME}

EXPOSE 5601

ENTRYPOINT ["/bin/bash"]
CMD ["-c", "bin/kibana -e ${KIBANA_ES_URL}"]
