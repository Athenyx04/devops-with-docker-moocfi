# We need Node 16. I found this from Docker Hub.
FROM node:16-alpine

EXPOSE 5000

WORKDIR /usr/src/app

# Copy all of the source code
COPY . .

# Add the environment information
ENV REACT_APP_BACKEND_URL http://localhost:8080

# Install all packages and build
RUN npm install && npm install -g serve && npm run build

# And finally the command to run the application
CMD ["serve", "-s", "-l", "5000", "build"]