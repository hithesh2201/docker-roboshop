FROM node:18
ENV MONGO=true
EXPOSE 8080
COPY package.json /opt/server/
COPY server.js /opt/server/
RUN npm install
CMD ["node", "server.js"]

