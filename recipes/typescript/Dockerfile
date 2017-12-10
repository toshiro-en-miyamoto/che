FROM eclipse/stack-base:ubuntu
RUN sudo apt-get update && \
    wget -qO- https://deb.nodesource.com/setup_8.x | sudo -E bash - && \
    sudo apt-get -y install nodejs && \
    sudo apt-get clean && \
    sudo apt-get -y autoremove && \
    sudo apt-get -y clean
RUN sudo npm install -g http-server typescript ts-node
EXPOSE 1337 3000 4200 5000 9000 8003
LABEL che:server:8003:ref=angular che:server:8003:protocol=http che:server:3000:ref=node-3000 che:server:3000:protocol=http che:server:9000:ref=node-9000 che:server:9000:protocol=http
# Command RUN: http
#   cd ${current.project.path}
#   http-server -p 9000
# Preview: http
#   ${server.9000/tcp}index.html
