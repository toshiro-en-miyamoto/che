FROM eclipse/stack-base:ubuntu
RUN sudo apt-get update && \
    wget -qO- https://deb.nodesource.com/setup_8.x | sudo -E bash - && \
    sudo apt-get -y install nodejs && \
    sudo apt-get clean && \
    sudo apt-get -y autoremove && \
    sudo apt-get -y clean
RUN sudo npm install -g @angular/cli
EXPOSE 4200 3000 9000
LABEL che:server:4200:ref=ng-serve che:server:4200:protocol=http che:server:3000:ref=node-3000 che:server:3000:protocol=http che:server:9000:ref=node-9000 che:server:9000:protocol=http
# [command] ng-serve:run
# cd ${current.project.path}
# ng serve --host 0.0.0.0
# OR npm start
# [preview URL] ${server.4200/tcp}
# Version as of Jan 15 2018
# node: 8.9.1
# npm: 5.5.1
# @angular/cli: 1.6.4
