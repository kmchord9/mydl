FROM tensorflow/tensorflow:latest-gpu

MAINTAINER kmchord9

ENV USER kmchord9
ENV HOME /home/${USER}
ENV SHELL /bin/bash

RUN useradd -m ${USER} &&\
    gpasswd -a ${USER} sudo &&\
    echo "${USER}:mypass" | chpasswd &&\
    sed -i.bak "s#${HOME}:#${HOME}:${SHELL}#" /etc/passwd

USER ${USER}
WORKDIR ${HOME}

CMD [ "/bin/bash" ]
