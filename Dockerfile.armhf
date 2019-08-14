ARG arch=armhf
FROM multiarch/alpine:${arch}-v3.9
#COPY qemu-arm-static /usr/bin/
#FROM alpine:3.9
COPY qemu-arm-static /usr/bin/
RUN apk add --no-cache curl jq

COPY docker-entrypoint /
ENTRYPOINT ["/docker-entrypoint"]

HEALTHCHECK --interval=5s CMD /docker-entrypoint healthcheck

CMD ["autoheal"]
