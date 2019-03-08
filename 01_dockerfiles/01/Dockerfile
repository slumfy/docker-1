FROM debian


EXPOSE 9987/udp 30033 10011
ENV TS3SERVER_LICENSE="accept"

RUN apt-get update \
	&& apt-get install wget bzip2 wget ca-certificates -y \
		&& adduser --disabled-password --gecos "" teamspeak

		WORKDIR /home/teamspeak

		RUN wget http://dl.4players.de/ts/releases/3.6.1/teamspeak3-server_linux_amd64-3.6.1.tar.bz2 \
			&& tar -jxf *.tar.bz2 && rm *.tar.bz2

			WORKDIR teamspeak3-server_linux_amd64

			CMD ["sh", "ts3server_minimal_runscript.sh"]

#docker run  -d --publish=9987:9987/udp --publish=30033:30033/tcp --publish=10011:10011/tcp --name test (id cont)
# docker logs pour recup la cle
