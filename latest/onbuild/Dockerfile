FROM friism/aspnet:latest
ENV SRC_DIR /src
RUN mkdir -p $SRC_DIR
WORKDIR $SRC_DIR
ONBUILD ADD NuGet.Config $SRC_DIR/
ONBUILD ADD project*.json $SRC_DIR/
ONBUILD RUN dnu restore
ONBUILD ADD . $SRC_DIR/
