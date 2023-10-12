FROM node


#ARG UID=20000
#ARG GID=20000
#RUN groupadd -g $GID dev \
#    && useradd -m -u $UID -g $GID dev
#ここが不要

RUN mkdir /frontend
WORKDIR /frontend
RUN npm install -g npm@latest && npm install create-next-app

RUN chown node /frontend
USER node
