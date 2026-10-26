FROM flyway/flyway:10-alpine

LABEL org.opencontainers.image.source="https://github.com/jesse-bugbash/dockerfile-fixtures" \
      com.datadoghq.image.source_path="jobs/db-migrations/Dockerfile"

COPY sql /flyway/sql
COPY flyway.conf /flyway/conf/flyway.conf
CMD ["migrate"]
