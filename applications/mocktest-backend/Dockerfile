FROM node
WORKDIR /app
COPY pyq-mocktest-backend/package.json /app
RUN npm install
COPY pyq-mocktest-backend /app
EXPOSE 8000
CMD ["node","src/index.js"]


