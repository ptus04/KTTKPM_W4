FROM node:18
WORKDIR /app

COPY package*.json ./
RUN npm ci --omit=dev

COPY index.mjs .
ENV NODE_ENV=production
EXPOSE 3000
CMD ["node", "index.mjs"]