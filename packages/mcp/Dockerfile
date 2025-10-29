# packages/mcp/Dockerfile
FROM node:18-alpine

# install git
RUN apk add --no-cache git

WORKDIR /app

# Copy package files
COPY package*.json ./

# Install dependencies
RUN npm install

# Copy application code
COPY . .

# Build the application
RUN npm run build

CMD ["node", "dist/index.js"]