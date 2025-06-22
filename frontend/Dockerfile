# Stage 1: Build
FROM node:18-alpine AS builder
WORKDIR /app
COPY package*.json ./
RUN npm install
COPY . .
RUN npm run build

# Stage 2: Run
FROM node:18-alpine
WORKDIR /app
<<<<<<< HEAD
COPY --from=builder /app/public ./public
=======
>>>>>>> feature/ci-pipeline
COPY --from=builder /app/.next ./.next
COPY --from=builder /app/package*.json ./
RUN npm install --production
EXPOSE 3000
CMD ["npm", "start"]
<<<<<<< HEAD
=======

>>>>>>> feature/ci-pipeline
