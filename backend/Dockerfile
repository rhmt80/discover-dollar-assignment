# backend/Dockerfile
FROM node:18-alpine

# Create app directory
WORKDIR /app

# Install dependencies
COPY package*.json ./
RUN npm install --production

# Copy the rest of the backend source code
COPY . .

# Environment variables (override in docker-compose if needed)
ENV PORT=8080
ENV MONGODB_URI=mongodb://mongo:27017/dd_db

EXPOSE 8080

# Start the backend server
CMD ["node", "server.js"]
