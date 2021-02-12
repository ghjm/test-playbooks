FROM registry.fedoraproject.org/fedora:33
RUN echo "max_parallel_downloads=10" >> /etc/dnf/dnf.conf && \
    echo "fastestmirror=True" >> /etc/dnf/dnf.conf && \
    dnf -y update && \
    dnf -y install nc && \
    dnf clean all
CMD ["/usr/bin/nc", "-l", "-k", "-p", "1234", "-e", "/usr/bin/echo Hello, world!"]
