FROM python:3.7-slim

RUN apt-get update && \
	apt-get install -y git nmap snmp wget nbtscan && \
        rm -rf /var/lib/apt/lists/* 

RUN git clone https://github.com/codingo/Reconnoitre.git recon

WORKDIR /recon

RUN pip install -r requirements.txt && python setup.py install

RUN useradd -m recon

RUN chown recon /recon

USER recon

ENTRYPOINT ["reconnoitre"]
