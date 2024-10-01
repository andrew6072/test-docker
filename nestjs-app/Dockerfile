FROM node:18-alpine

WORKDIR /app

# Copy only package.json and package-lock.json
COPY package*.json ./

# Install dependencies
RUN npm ci

# Copy the rest of the application
COPY . .

# Expose the port your application runs on
EXPOSE 3000

# Run the application
CMD ["npm", "run", "start:prod"]