# Use Node base image
FROM node:18

# Set working directory
WORKDIR /app

# Copy package.json and install deps
COPY package*.json ./
RUN npm install

# Copy source code
COPY . .

# Build NestJS
RUN npm run build

# Expose backend port
EXPOSE 5000

# Run the app
CMD ["npm", "run", "start:prod"]

