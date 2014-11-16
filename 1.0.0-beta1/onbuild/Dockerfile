FROM microsoft/aspnet:1.0.0-beta1

RUN mkdir -p /usr/src/app
WORKDIR /usr/src/app

ONBUILD COPY project.json /usr/src/app/
ONBUILD RUN kpm restore

ONBUILD COPY . /usr/src/app/

ENTRYPOINT [ "k" ]
CMD [ "kestrel" ]
