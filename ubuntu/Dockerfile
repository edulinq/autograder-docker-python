FROM ghcr.io/edulinq/grader.base:0.1.1-ubuntu22.04

ENV DEBIAN_FRONTEND=noninteractive
RUN apt-get update

RUN apt-get install -y \
    python3-pip \
    python3-setuptools

COPY requirements.txt /autograder/
COPY scripts /autograder/scripts

RUN pip3 install -r /autograder/requirements.txt

WORKDIR /autograder

CMD ["/autograder/scripts/run_grader.sh"]
