FROM node:23-alpine
COPY app.js /app.js
COPY html/ /html
EXPOSE $PORT 8000
ENTRYPOINT [ "node", "app.js" ]