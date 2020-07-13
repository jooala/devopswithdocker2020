FROM ubuntu:16.04 

WORKDIR /mydir

RUN apt-get update && apt-get install -y curl
COPY scripts.sh .
RUN chmod +x scripts.sh
CMD ./scripts.sh

# commands:
# docker build -t curler .
# docker run -it curler