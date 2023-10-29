FROM python:3.11.5

COPY pyproject.toml .
COPY poetry.lock .

RUN set -ex \
 && apt-get update -yqq \
 && ACCEPT_EULA=Y \
 && apt-get install --no-install-recommends -yqq \
      unixodbc-dev \
      libpq-dev \
      g++ \
      git \
      rsync \
      freetds-dev \
      freetds-bin \
      tdsodbc \
 && curl https://pyenv.run | bash \
 && pip3 install poetry
RUN poetry install