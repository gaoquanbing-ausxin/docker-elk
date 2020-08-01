ARG ELK_VERSION

# https://www.docker.elastic.co/
FROM docker.elastic.co/elasticsearch/elasticsearch:${ELK_VERSION}

# Add your elasticsearch plugins setup here
# Example: RUN elasticsearch-plugin install analysis-icu

WORKDIR /usr/share/elasticsearch/plugins/ik
RUN yum install -y wget unzip && \
    wget https://github.com/medcl/elasticsearch-analysis-ik/releases/download/v7.3.2/elasticsearch-analysis-ik-7.3.2.zip && \
    unzip elasticsearch-analysis-ik-7.3.2.zip && \
    rm -rf elasticsearch-analysis-ik-7.3.2.zip