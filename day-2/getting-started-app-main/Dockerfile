FROM node:22-alpine

WORKDIR /app
# Copy from current working directory into docker containers CWD eg. /app
COPY . .

RUN yarn install --production

CMD ["node", "src/index.js"]
# ENTRYPOINT is the lower level command that can be used instead of CMD, ENTRYPOINT points to the bash shell, 
# which executes the params/arguments sent in by CMD (CMD can't be overwritten running outside of the image but entrypoint can)

EXPOSE 3000
