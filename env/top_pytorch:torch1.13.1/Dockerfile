FROM pytorch/pytorch:1.13.1-cuda11.6-cudnn8-runtime
RUN apt-get update && \
    apt-get install sshfs -y && \
    apt-get install tmux -y && \
    pip install --upgrade pip
WORKDIR /mount
VOLUME /mount
COPY ./requirements.txt /mount/requirements.txt
RUN pip install --no-cache-dir -r requirements.txt

# docker build . -t image:version
