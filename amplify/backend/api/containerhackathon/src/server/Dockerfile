FROM public.ecr.aws/bitnami/node:16.13.0-prod-debian-10-r33

ENV PORT=8080
EXPOSE 8080

WORKDIR /usr/src/app

COPY package*.json ./
RUN npm install && npm rebuild --verbose sharp
COPY . .

CMD [ "npm", "run", "start" ]
