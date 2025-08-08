FROM node:14

WORKDIR /app

COPY package*.json ./
RUN npm install

COPY . .

# Install wait-port (or curl-based wait script)
RUN npm install -g wait-port

EXPOSE 5000

CMD wait-port db:5432 && npm start