# frontend/Dockerfile
FROM node:18-alpine

WORKDIR /app

# Install dependencies
COPY package*.json ./
RUN npm install

# Copy source
COPY . .

# Angular dev server will listen on 8081
EXPOSE 8081

# Make sure "start" script runs ng serve on 0.0.0.0
CMD ["npm", "start"]
