FROM node:slim

ARG HOME_DIR=/root
ARG TUTORIAL_DIR=${HOME_DIR}/tutorial
RUN mkdir -p ${TUTORIAL_DIR}/

WORKDIR ${TUTORIAL_DIR}
COPY public ${TUTORIAL_DIR}/public
COPY src ${TUTORIAL_DIR}/src

ENV CHOKIDAR_USEPOLLING=true
RUN touch ${TUTORIAL_DIR}/src/app.css

COPY package.json .
COPY package-lock.json .

RUN npm install
RUN npm install @patternfly/react-core
RUN npm install @patternfly/react-tokens
RUN npm install @patternfly/react-charts
RUN npm install @patternfly/react-table

CMD ["npm", "start"]
