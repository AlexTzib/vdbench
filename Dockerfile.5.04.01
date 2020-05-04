FROM openjdk:8-jre
RUN apt-get update && \
    apt-get install -y --no-install-recommends csh && \
    rm -rf /var/lib/apt/lists/*
RUN curl -L https://app.box.com/s/o9cnhr2ykku16l4imf24n9a3ogz5aa7q -o vdbench501.zip && \
    mkdir vdbench && cd vdbench && \
    unzip ../vdbench501.zip && rm ../vdbench501.zip && \
    mkdir -p /opt && mv ../vdbench /opt
WORKDIR /opt/vdbench
ENTRYPOINT ["/opt/vdbench/vdbench"]
