FROM solr:7

LABEL maintainer="Solr Drupal"
LABEL repository="https://github.com/saidatom/solr"

RUN mkdir /var/drupal

RUN /opt/docker-solr/scripts/precreate-core drupal_search_api
RUN /opt/docker-solr/scripts/precreate-core drupal_apachesolr

VOLUME /var/solr
EXPOSE 8983
WORKDIR /opt/solr
USER $SOLR_USER

ENTRYPOINT ["docker-entrypoint.sh"]
CMD ["solr-foreground"]