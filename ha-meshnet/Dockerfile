ARG BUILD_FROM
FROM $BUILD_FROM

# Install dependencies
RUN apt-get update && apt-get install -y \
    curl \
    sudo

# Install NordVPN CLI
RUN curl -sSL https://downloads.nordcdn.com/apps/linux/install.sh | sh

# Set environment variables for NordVPN credentials
ENV NORDVPN_USER=<your_nordvpn_username>
ENV NORDVPN_PASSWORD=<your_nordvpn_password>

# Copy data for add-on
COPY rootfs/etc/services.d/run /run.sh
COPY rootfs/usr/bin/meshnet /usr/bin/meshnet
RUN chmod a+x /run.sh /usr/bin/meshnet

CMD [ "/run.sh" ]
