#docker build -t cip-rockwell-device .
#docker run -it --net=host -d --name rockwell cip-rockwell-device
FROM python:3.8.19-alpine3.20
WORKDIR /
RUN python3 -m pip install cpppo
EXPOSE 44818
CMD [ "python3", "-m", "cpppo.server.enip",  "-v",  "scada=DINT[1000]", "real=REAL" ]
