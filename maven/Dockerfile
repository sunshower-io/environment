FROM sunshower/sunshower-base:1.0.0

ENV PROJECT_NAME=environment
ENV MVN_REPO_USERNAME ""
ENV MVN_REPO_PASSWORD ""
RUN env
COPY ./environment /home/sunshower/$PROJECT_NAME
WORKDIR /home/sunshower/$PROJECT_NAME
RUN mvn \
--settings=settings/settings.xml \
clean install deploy

ENTRYPOINT /bin/bash