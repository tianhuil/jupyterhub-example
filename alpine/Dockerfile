FROM mhart/alpine-node:8

# Install Python3
RUN apk add --no-cache python3-dev && \
    python3 -m ensurepip && \
    rm -r /usr/lib/python*/ensurepip && \
    pip3 install --upgrade pip setuptools && \
    if [ ! -e /usr/bin/pip ]; then ln -s pip3 /usr/bin/pip ; fi && \
    rm -r /root/.cache

RUN npm install -g configurable-http-proxy

RUN pip3 install jupyterhub

WORKDIR /app

RUN jupyterhub --generate-config

EXPOSE 8000 8001
CMD ["jupyterhub"]
