FROM ubuntu:22.04

RUN apt-get update \
&& apt-get install -y ca-certificates curl gnupg \
&& curl -fsSL https://deb.nodesource.com/gpgkey/nodesource-repo.gpg.key | gpg --dearmor -o /etc/apt/keyrings/nodesource.gpg \
&& echo "deb [signed-by=/etc/apt/keyrings/nodesource.gpg] https://deb.nodesource.com/node_20.x nodistro main" | tee /etc/apt/sources.list.d/nodesource.list \
&& apt-get update \
&& apt-get install nano nodejs -y

ARG ENV=dev

LABEL author="Jacques"
LABEL email="crunksw@gmail.com"

ENV ENV=${ENV}

#définition du path-folder
WORKDIR /var/www/html

#copie des fichiers dans le container
COPY index.js .


# CMD [ "node", "index.js" ]


