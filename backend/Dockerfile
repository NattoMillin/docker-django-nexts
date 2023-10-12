FROM python:3
ENV PYTHONUNBUFFERED 1

ARG UID=20000
ARG GID=20000
RUN groupadd -g $GID dev \
    && useradd -m -u $UID -g $GID dev
#ユーザーを追加。

RUN mkdir /backend
WORKDIR /backend
#user指定前にmkdirをする必要があり、その状態でchownを行わなければならない。

ADD requirements.txt /backend/
RUN pip install -r requirements.txt

RUN chown dev /backend
USER dev
