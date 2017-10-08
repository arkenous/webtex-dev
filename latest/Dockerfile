## -*- docker-image-name: "k3nsuk3/webtex-dev" -*-
FROM k3nsuk3/arch-base:latest
MAINTAINER Kensuke Kousaka <k@k3n.link>

RUN pacman -Syu --noconfirm python jre8-openjdk-headless texlive-langcjk texlive-fontsextra poppler &> /dev/null
User user

WORKDIR /home/user/

RUN curl -L -O --silent https://bootstrap.pypa.io/get-pip.py && \
  python get-pip.py --user > /dev/null && \
  rm -f get-pip.py
ENV PATH $PATH:/home/user/.local/bin
COPY pip-requirements.txt /home/user/
RUN pip install --user -r /home/user/pip-requirements.txt > /dev/null && rm -f /home/user/pip-requirements.txt

VOLUME ["/home/user/WebTeX"]

ENV PATH $PATH:/home/user/WebTeX/redpen/bin
