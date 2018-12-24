FROM postgres:11

RUN apt-get update && apt-get install -y postgresql-11-cron \
      postgresql-11-cron-dbgsym \
      postgresql-11-ip4r \
      postgresql-11-ip4r-dbgsym \
      postgresql-11-jsquery \
      postgresql-11-jsquery-dbgsym \
      postgresql-11-pgq3 \
      postgresql-11-pgq3-dbgsym \
      postgresql-11-pgrouting \
      postgresql-11-pgrouting-dbgsym \
      postgresql-11-pgrouting-doc \
      postgresql-11-pgrouting-scripts \
      postgresql-11-plsh \
      postgresql-11-plsh-dbgsym \
      postgresql-11-postgis-2.5 \
      postgresql-11-postgis-2.5-dbgsym \
      postgresql-11-postgis-2.5-scripts \
      postgresql-11-unit \
      postgresql-11-unit-dbgsym \
    && rm -rf /var/lib/apt/lists/*
