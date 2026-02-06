FROM ghcr.io/edulinq/grader.base:0.1.1-alpine3.20.3

RUN apk update
RUN apk add --no-cache \
    python3 \
    py3-pip

COPY requirements.txt /autograder/
COPY scripts /autograder/scripts

RUN pip3 install --break-system-packages -r /autograder/requirements.txt

WORKDIR /autograder

CMD ["/autograder/scripts/run_grader.sh"]
