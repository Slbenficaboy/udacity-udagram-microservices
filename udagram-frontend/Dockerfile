FROM node:13

# Create app directory
WORKDIR /usr/src/app

# Install app dependencies by copying
# package.json and package-lock.json
COPY package*.json ./

# Install dependencies
RUN npm install
RUN npm install -g ionic

# Copy app source
COPY . .

# Build the frontend
RUN ionic build

# Serve the frontend
EXPOSE 8100
CMD [ "ionic", "serve"]