FROM ubuntu
COPY . ./bigdata
WORKDIR ./bigdata

RUN apt update
RUN apt install python3 python3-pip git python3-venv -y

RUN python3 -m venv /opt/MyEnv

RUN . /opt/MyEnv/bin/activate && pip3 install -r Requirements.txt

EXPOSE 8000
CMD ["jupyter", "notebook", "--ip=0.0.0.0", "--port=8000", "--allow-root"]
