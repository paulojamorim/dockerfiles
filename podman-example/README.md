## To construct the image:

```
podman build -t my_image_name .
```

*Be patient as it takes a little while.*

## To run

Python code inside the container using the previously created image, you can follow these steps:

```
podman run -it --rm -v ./:/code -e NVIDIA_VISIBLE_DEVICES=0 my_image_name python3 main.py /code/file_read.txt
```

* ```-v ./:/code``` (Mapping current folder to /code into container)
* ```-e NVIDIA_VISIBLE_DEVICES=0,1``` (uses GPU 0 and 1)