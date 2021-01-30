# one set of the layer
# as - tags the name of the phase
FROM node:alpine as builder
WORKDIR "/app"
COPY package.json .
RUN npm install
COPY . .
# build folder will be created in the working directory
RUN npm run build

# only copy the needed information from the first set of the layer
# this will help to reduce the size of the image
FROM nginx
# copy over sth from different phase
COPY --from=builder /app/build /usr/share/nginx/html

