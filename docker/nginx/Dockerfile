FROM alpine AS builder

RUN mkdir /sock \
    && chown -R nobody:nobody /sock


FROM nginxinc/nginx-unprivileged:stable-alpine-slim

COPY --chown=nobody --from=builder /sock /sock

VOLUME ["/sock"]

USER nobody