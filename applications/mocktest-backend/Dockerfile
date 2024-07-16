FROM node
WORKDIR /app
COPY pyq-mock-backend/package.json /app
RUN npm install
COPY pyq-mock-backend /app
EXPOSE 8000
CMD ["node","src/index.js"]


