# Step 1: Use an official Node.js runtime as the base image (alpine for a smaller image)
FROM node:18-alpine

# Step 2: Set the working directory inside the container
WORKDIR /app

# Step 3: Copy package.json and package-lock.json (if available) into the container
COPY package*.json ./

# Step 4: Install dependencies (use npm ci for faster, clean install if package-lock is present)
RUN npm install

# Step 5: Copy the rest of the application code into the container
COPY . .

# Step 6: Set the environment variable to address OpenSSL issue on Node 17+ (use legacy OpenSSL provider)
ENV NODE_OPTIONS=--openssl-legacy-provider

# Step 7: Expose the port the app will run on
EXPOSE 3000

# Step 8: Define the command to run the application
CMD ["npm", "start"]
