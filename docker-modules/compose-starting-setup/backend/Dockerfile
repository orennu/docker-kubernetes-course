FROM node

WORKDIR /app

COPY package.json .

RUN npm install

COPY . .

EXPOSE 80

ENV DB_USER=root
ENV DB_PASS=secret

RUN chown -R node:node /app

CMD ["npm", "start"]