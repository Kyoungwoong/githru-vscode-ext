FROM node:18-alpine

# Install git
RUN apk add --no-cache git

WORKDIR /app

# Copy package files first (for better Docker layer caching)
COPY package*.json ./

# Install dependencies (both prod and dev for build step)
RUN npm install

# Copy source code
COPY . .

# Build the application (requires devDependencies: copyfiles, typescript)
RUN npm run build

# Run the server
CMD ["node", "dist/server.js"]