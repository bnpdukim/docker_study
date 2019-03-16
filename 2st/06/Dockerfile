FROM docker/whalesay

RUN mv /usr/local/share/cows/default.cow /usr/local/share/cows/orig-default.cow

COPY ./cheese.cow /usr/local/share/cows/
RUN ln -sv /usr/local/share/cows/cheese.cow /usr/local/share/cows/default.cow
RUN apt-get -y update && apt-get install -y fortune


CMD /usr/games/fortune -a | cowsay
