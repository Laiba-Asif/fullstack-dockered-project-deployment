
FROM node:18-alpine AS build

WORKDIR /app

COPY package*.json ./
RUN npm ci --omit=dev && npm cache clean --force

COPY . .

FROM node:18-alpine

WORKDIR /app

RUN addgroup -S nodejs && adduser -S nodejs -G nodejs

COPY --from=build --chown=nodejs:nodejs /app /app

USER nodejs

EXPOSE 3500

CMD ["node", "server.js"]

