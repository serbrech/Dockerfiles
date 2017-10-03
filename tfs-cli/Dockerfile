FROM node
LABEL maintainer "Stephane Erbrech <sterbrec@microsoft.com>"

# > docker run -it sterbrec/tfs-cli login --service-url sterbrec.visualstudio.com --token hfuhrufhre32459892uroiejd43ut8uf9433535fr
# > docker commit (docker ps --latest -q) local/tfx
# > docker run --rm local/tfx workitem show --work-item-id 1000

# Obviously, Don't push your logged in container...

ENV HOME /home/user
RUN useradd --create-home --home-dir $HOME user \
&& chown -R user:user $HOME

RUN npm install -g tfx-cli

WORKDIR $HOME
USER user

ENTRYPOINT ["tfx"]
CMD ["version"]

