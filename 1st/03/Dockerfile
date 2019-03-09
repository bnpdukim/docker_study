FROM docker/whalesay

#RUN mv /usr/share/cowsay/cows/default.cow /usr/share/cowsay/cows/orig-default.cow

COPY ./cheese.cow /usr/share/cowsay/cows/
RUN ln -sv /usr/share/cowsay/cows/cheese.cow /usr/share/cowsay/cows/default.cow
RUN apt-get -y update && apt-get install -y fortune


CMD /usr/games/fortune -a | cowsay
