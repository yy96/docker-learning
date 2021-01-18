# Specify a base image
FROM node:alpine

# Install some dependencies
# Set working directory to avoid accidently overwriting another file at root
WORKDIR /usr/app
COPY ./package.json ./
RUN npm install
COPY ./ ./

# Default command
CMD ["npm", "start"]