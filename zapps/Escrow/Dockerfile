FROM node:18.19

WORKDIR /app


COPY ./package.json ./
COPY circuits ./circuits
COPY config ./config
COPY build/contracts ./build/contracts
COPY orchestration ./orchestration
COPY proving-files ./proving-files
RUN npm i
COPY bn.js ./node_modules/number-to-bn/node_modules/bn.js/lib
EXPOSE 3000
CMD ["node", "orchestration/api.mjs"]