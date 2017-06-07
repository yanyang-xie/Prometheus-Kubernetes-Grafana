FROM yanyang/vod-simulator

ADD ./jmx_prometheus_javaagent-0.9.jar /root
ADD ./sample-config.yml /root

WORKDIR /root

EXPOSE 8081

WORKDIR /root/vod-simulator
#ENTRYPOINT ["java", "-cp", "/root/vod-simulator/conf:/root/vod-simulator/conf-golden:/root/vod-simulator/lib/*", "com.thistech.vodsimulator.VODSimulatorServer"]
ENTRYPOINT ["java", "-cp", "/root/vod-simulator/conf:/root/vod-simulator/conf-golden:/root/vod-simulator/lib/*", "-javaagent:/root/jmx_prometheus_javaagent-0.9.jar=1234:/root/sample-config.yml",   "com.thistech.vodsimulator.VODSimulatorServer"]
