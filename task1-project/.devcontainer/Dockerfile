FROM python:3.11.5

COPY app/requirements.txt .

RUN set -ex \
 && apt-get update -yqq \
 && ACCEPT_EULA=Y apt-get install --no-install-recommends -yqq \
      unixodbc-dev \
      libpq-dev \
      g++ \
      git \
      rsync \
      freetds-dev \
      freetds-bin \
      tdsodbc \
 && pip3 install flake8 pylint autopep8 \
 && pip3 install -r requirements.txt