FROM node:22-alpine AS installer-stage

WORKDIR /app

# Package json is copied first to cache npm install run
COPY package*.json .
RUN npm install

# Rest of files are only copied after to not uncache the npm install.
COPY . .

RUN npm run build

FROM nginx:latest AS final-stage

COPY --from=installer-stage /app/build /usr/share/nginx/html