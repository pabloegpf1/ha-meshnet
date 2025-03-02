ARG BUILD_FROM
FROM $BUILD_FROM

COPY rootfs/etc/services.d/run /run.sh
RUN chmod a+x /run.sh

CMD [ "/run.sh" ]
