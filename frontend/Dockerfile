# Use Node base image
FROM node:20-alpine

# Set working directory
WORKDIR /app

# Copy package files and install dependencies
COPY package*.json ./
RUN npm install

# Copy rest of the frontend code
COPY . .

# Expose frontend port
EXPOSE 3000

# Start the React app
CMD ["npm", "start"]

ENV CHOKIDAR_USEPOLLING=true
ENV BROWSER=none
ENV NODE_ENV=development