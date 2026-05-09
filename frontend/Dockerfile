FROM node:18

WORKDIR /app

COPY package*.json ./

RUN npm ci

COPY . .
RUN npm run build && mv build build_result

CMD ["sh", "-c", "cp -r build_result/. /app/build/ && tail -f /dev/null"]
