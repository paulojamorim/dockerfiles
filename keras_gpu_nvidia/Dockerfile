#based from https://gitlab.com/nvidia/cuda/blob/ubuntu14.04/7.5/runtime/cudnn5/Dockerfile

ARG repository="nvidia/cuda"
FROM ${repository}:8.0-devel-ubuntu16.04

LABEL maintainer "Paulo Henrique Junqueira Amorim <paulojamorim@gmail.com>"

RUN echo "deb https://developer.download.nvidia.com/compute/machine-learning/repos/ubuntu1604/x86_64 /" > /etc/apt/sources.list.d/nvidia-ml.list

ENV CUDNN_VERSION 6.0.21

LABEL com.nvidia.cudnn.version="${CUDNN_VERSION}"

RUN apt-get update && apt-get install -y --no-install-recommends \
            libcudnn6=$CUDNN_VERSION-1+cuda8.0 \
            libcudnn6-dev=$CUDNN_VERSION-1+cuda8.0 \
            bzip2 g++ gcc git graphviz \
            libgl1-mesa-glx libhdf5-dev openmpi-bin \
            python-dev python-pip python-setuptools python-vtk6 \ 
            python-vtkgdcm python-gdcm wget \
	        tmux ipython vim && \
            rm -rf /var/lib/apt/lists/* && \
            pip install --upgrade pip==9.0.3 && \
            pip install h5py==2.6.0 tensorflow-gpu==1.4.0 \
                Keras==2.0.6 matplotlib==2.0.2 opencv-python==3.2.0.7 \
                Pillow==5.1.0 scikit-image==0.13.0 scikit-learn==0.17.1 \
		scipy==0.19.1 configparser==3.5.0 && \
            rm -rf /var/lib/apt/lists/* && \
            apt-get clean
            
WORKDIR /src
