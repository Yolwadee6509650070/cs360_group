# Use the official Node.js 16 image as base 
FROM node:16


# Set the working directory inside the container
WORKDIR /app

# Copy package.json and package-lock.json (if available)
COPY package*.json yarn.lock ./

# Install dependencies
RUN yarn install

# Copy the entire application source code
COPY . .

# Expose the port your app runs on
EXPOSE 3000

# Start the app 
CMD ["sh", "-c", "yarn build && yarn start"]