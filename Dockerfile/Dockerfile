FROM jenkins/jenkins:lts
# if we want to install via apt
USER root
RUN apt-get clean
RUN apt-get update --fix-missing
RUN apt-get install -y make --fix-missing
RUN apt-get install -y g++ --fix-missing
# drop back to the regular jenkins user - good practice
USER jenkins






