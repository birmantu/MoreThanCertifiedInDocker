FROM nodered/node-red

RUN npm install node-red-contrib-influxdb

COPY flows_cred.json /data/flows_cred.json
COPY settings.js /data/settings.js
COPY flows.json /data/flows.json