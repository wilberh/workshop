FROM openjdk:8

# we have this locally instead of downloading it because of conference wi-fi considerations
COPY gradle-4.9-bin.zip .
RUN unzip gradle-4.9-bin.zip -d /opt \
    && rm gradle-4.9-bin.zip

ENV GRADLE_HOME /opt/gradle-4.9
ENV PATH $PATH:/opt/gradle-4.9/bin


