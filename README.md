# OpenSourceComputerVision

Open Source Computer Vision with TensorFlow, MiniFi, Apache NiFi, OpenCV, Apache Tika and Python   For processing images from IoT devices like Raspberry Pis, NVidia Jetson TX1, NanoPi Duos and more which are equipped with attached cameras or external USB webcams, we use Python to interface via OpenCV and PiCamera.    From there we run image processing at the edge on these IoT device using OpenCV and TensorFlow to determine attributes and image analytics.   A pache MiniFi coordinates running these Python scripts and decides when and what to send from that analysis and the image to a remote Apache NiFi server for additional processing.     At the Apache NiFi cluster in the cluster it routes the images to one processing path and the JSON encoded metadata to another flow.    The JSON data (with it's schema referenced from a central Schema Registry) is routed and routed using Record Processing and SQL, this data in enriched and augment before conversion to AVRO to be send via Apache Kafka to SAM.   Streaming Analytics Manager then does deeper processing on this stream and others including weather and twitter to determine what should be done on this data.  

References 

* https://community.hortonworks.com/articles/103863/using-an-asus-tinkerboard-with-tensorflow-and-pyth.html 
* https://community.hortonworks.com/articles/118132/minifi-capturing-converting-tensorflow-inception-t.html 
* https://github.com/tspannhw/rpi-noir-screen 
* https://community.hortonworks.com/articles/77988/ingest-remote-camera-images-from-raspberry-pi-via.html 
* https://community.hortonworks.com/articles/107379/minifi-for-image-capture-and-ingestion-from-raspbe.html 
* https://community.hortonworks.com/articles/58265/analyzing-images-in-hdf-20-using-tensorflow.html



pb.py 

License
MIT

Code used from Mask R-CNN by Matterport, Inc. (MIT-Licensed), with minor alterations and copyright notices retained.

