FROM "ubuntu:bionic"
RUN apt-get update && yes | apt-get upgrade
RUN mkdir -p /tensorflow/models
RUN apt-get install -y git python3-pip
RUN pip3 install --upgrade pip
RUN pip3 uninstall tensorflow
RUN pip3 install tensorflow==1.14
RUN apt-get install -y protobuf-compiler python3-pil python3-lxml
RUN pip3 install jupyter
RUN pip3 install matplotlib
RUN pip install opencv-python-headless
WORKDIR /tensorflow/models/research
RUN pip3 install streamlit==0.52.2
RUN pip3 install onnxruntime==0.5.0
RUN pip3 install torch==1.1.0
RUN pip3 install scikit-image==0.14.2
RUN pip3 install flask
