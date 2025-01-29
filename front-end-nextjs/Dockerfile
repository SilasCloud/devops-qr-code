# Use the official lightweight Node.js 18 image
FROM node:18-alpine AS base

# Set the working directory in the container
WORKDIR /app

# Copy the package files
COPY package.json yarn.lock* package-lock.json* pnpm-lock.yaml* ./

# Copy the install-dependencies.sh script
COPY install-dependencies.sh ./

# Install dependencies using the script
<<<<<<< HEAD
RUN ./install-dependencies.sh
=======
RUN chmod +x ./install-dependencies.sh && ./install-dependencies.sh
>>>>>>> 9db5a81 (Moved Terraform files into the infrastructure folder)

# Copy the rest of the application code
COPY . .

<<<<<<< HEAD
=======
# Run the Next.js build step
RUN npm run build

# Expose the build folder
RUN mkdir -p .next

# Copy the .next folder (to avoid context issues)
COPY .next ./.next

>>>>>>> 9db5a81 (Moved Terraform files into the infrastructure folder)
# Expose the application port
EXPOSE 3000

# Start the application
CMD ["npm", "start"]
<<<<<<< HEAD

# Build the Next.js app
RUN npm run build

# Expose the build folder
COPY .next ./.next
=======
>>>>>>> 9db5a81 (Moved Terraform files into the infrastructure folder)
