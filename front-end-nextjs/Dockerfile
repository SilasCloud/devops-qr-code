# Use the official lightweight Node.js 18 image
FROM node:18-alpine AS base

# Set the working directory in the container
WORKDIR /app

# Copy the package files
COPY package.json yarn.lock* package-lock.json* pnpm-lock.yaml* ./

# Copy the install-dependencies.sh script
COPY install-dependencies.sh ./

# Install dependencies using the script
RUN ./install-dependencies.sh

# Copy the rest of the application code
COPY . .

# Expose the application port
EXPOSE 3000

# Start the application
CMD ["npm", "start"]

# Build the Next.js app
RUN npm run build

# Expose the build folder
COPY .next ./.next
