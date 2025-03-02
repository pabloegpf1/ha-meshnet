FROM debian:latest

# Install dependencies
RUN apt-get update && apt-get install -y \
    curl \
    sudo

# Install NordVPN CLI
RUN curl -sSL https://downloads.nordcdn.com/apps/linux/install.sh | sh

# Copy data for add-on
COPY rootfs/etc/services.d/run /run.sh
COPY rootfs/usr/bin/meshnet /usr/bin/meshnet
RUN chmod a+x /run.sh /usr/bin/meshnet

CMD [ "/run.sh" ]
