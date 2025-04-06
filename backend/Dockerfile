# Use the official Node.js image.
FROM node:19.7.0

# Set the working directory inside the container.
WORKDIR /usr/src/app

# Copy package.json and yarn.lock
COPY package.json yarn.lock ./

# Install dependencies using Yarn
RUN yarn install

# Copy the rest of your application files
COPY . .

# Set environment to production (can be overridden at runtime)
ENV NODE_ENV=production

# Expose the port your app runs on
EXPOSE 4000

# Run the application using Yarn
CMD ["yarn", "start"]
