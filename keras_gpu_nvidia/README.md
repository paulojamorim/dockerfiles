Dockerfile to generate image based Ubuntu 16.04 NVidia cuDNN 6.0 and Cuda 8.0.

# Includes #

- h5py 2.6.0
- tensorflow-gpu 1.4.0
- Keras 2.0.6 
- matplotlib 2.0.2 
- opencv-python 3.2.0.7
- Pillow 5.1.0 
- scikit-image 0.13.0 
- scikit-learn 0.17.1
- ipython
- tmux
- git
- VTK 5.10.1
- GDCM

# To run #

You need to install nvidia-docker

- Debian based host:

`curl -s -L https://nvidia.github.io/nvidia-docker/gpgkey | \
   sudo apt-key add -
distribution = $ (. / etc / os-release; echo $ ID $ VERSION_ID)
curl -s -L https://nvidia.github.io/nvidia-docker/$distribution/nvidia-docker.list | \
   sudo tee /etc/apt/sources.list.d/nvidia-docker.list
sudo apt-get update`

`sudo apt-get install nvidia-docker`

- RHEL based host:

`distribution = $ (. / etc / os-release; echo $ ID $ VERSION_ID)
curl -s -L https://nvidia.github.io/nvidia-docker/$distribution/nvidia-docker.repo | \
   sudo tee /etc/yum.repos.d/nvidia-docker.repo`

Finally to run:
`nvidia-docker run -ti paulojamorim/keras_gpu_nvidia`
