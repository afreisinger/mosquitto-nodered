ARG NODERED_VERSION

FROM nodered/node-red:${NODERED_VERSION}
RUN npm install node-red-dashboard \
    npm install node-red-contrib-influxdb \
    npm install node-red-node-openweathermap \
    npm install node-red-node-arduino
#WORKDIR /data
#COPY flows.json /data/flows.json
WORKDIR /usr/src/node-red