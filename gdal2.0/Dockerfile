FROM "ubuntu:bionic"
RUN apt-get update && yes | apt-get upgrade
RUN mkdir -p /testdocker
RUN apt-get install -y software-properties-common
RUN add-apt-repository -y ppa:ubuntugis/ppa
RUN apt -y upgrade
RUN apt -y install gdal-bin python3-gdal

RUN apt-get install -y git python3-pip
RUN pip3 install --upgrade pip
RUN pip3 install jupyter
RUN pip3 install matplotlib
RUN pip install opencv-python-headless
RUN jupyter notebook --generate-config --allow-root
RUN echo "c.NotebookApp.password = u'sha1:6a3f528eec40:6e896b6e4828f525a6e20e5411cd1c8075d68619'" >> /root/.jupyter/jupyter_notebook_config.py
EXPOSE 8888
CMD ["jupyter", "notebook", "--allow-root", "--notebook-dir=/testdocker", "--ip=0.0.0.0", "--port=8888", "--no-browser"]

