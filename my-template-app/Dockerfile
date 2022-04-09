FROM node:16.14.2 AS builder
WORKDIR /usr/src/app
COPY package.json package-lock.json ./
RUN npm install
COPY . .
RUN npm run build

FROM nginx:latest

# Copy the build output to replace the default nginx contents.
COPY --from=builder /usr/src/app/dist/my-template-app /usr/share/nginx/html

# Expose port 80
EXPOSE 80