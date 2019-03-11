FROM mono:5

WORKDIR /opt
RUN curl http://dist.opensimulator.org/opensim-0.9.0.1.tar.gz -s | tar xzf - && mv opensim-0.9.0.1 opensim
EXPOSE 9000
WORKDIR /opt/opensim/bin

CMD [ "mono",  "./OpenSim.exe" ]
