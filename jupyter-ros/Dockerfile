FROM ros:melodic-robot

WORKDIR /opt
RUN apt-get update -y
RUN apt-get upgrade -y
RUN apt-get install -y wget vim curl git

# install pip
RUN wget https://bootstrap.pypa.io/get-pip.py
RUN python get-pip.py

RUN pip install jupyter bqplot pyyaml jupyros jupyterlab
RUN jupyter nbextension enable --py --sys-prefix jupyros

# install nodejs npm
RUN apt-get remove -y --purge nodejs npm
RUN apt-get clean -y
RUN apt-get autoclean -y
RUN apt-get install -f -y
RUN apt-get autoremove -y
RUN curl -sL https://deb.nodesource.com/setup_8.x | bash -
RUN apt-get install -y nodejs
RUN curl -sL https://dl.yarnpkg.com/debian/pubkey.gpg | apt-key add -
RUN apt-get update && apt-get install -y yarn
