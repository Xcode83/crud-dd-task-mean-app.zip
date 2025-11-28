FROM node:18-alpine

WORKDIR /app

# Install deps
COPY package*.json ./
RUN npm install --production

# Copy source
COPY . .

# Environment
ENV PORT=8080

# This is used by backend/app/config/db.config.js
ENV MONGO_URL=mongodb://mongo:27017/dd_db

EXPOSE 8080

CMD ["node", "server.js"]
