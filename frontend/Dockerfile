# BUILD PHASE
# as - tags the name of the phase
FROM node:alpine as builder
WORKDIR "/app"
COPY package.json .
RUN npm install
COPY . .
# build folder will be created in the working directory
RUN npm run build

# RUN PHASE
# only copy the needed information from the first phase
# this will help to reduce the size of the image
FROM nginx
# for elastic beanstalk to map the port to this number automatically
EXPOSE 80
# copy over the result of 'npm run build' from BUILD PHASE
COPY --from=builder /app/build /usr/share/nginx/html

