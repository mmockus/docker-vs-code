# Use the linuxserver/code-server image as the base image
FROM linuxserver/code-server:latest

# Install SSH server
RUN apt-get update && \
    apt-get install -y openssh-server && \
    rm -rf /var/lib/apt/lists/*

# Expose SSH port
EXPOSE 22

# Start SSH service and code-server
CMD ["/usr/sbin/sshd", "-D"]
