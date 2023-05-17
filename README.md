# Setting Up Software

1.) Clone Repository:

```
git clone https://github.com/ecd1012/rpi_road_object_detection.git
```

2.) Change directory to source code:

```
cd rpi_road_object_detection
```

3.) Open command prompt and make sure pi is up to date:

```
sudo apt-get update && sudo apt-get upgrade
```

4.) Install virtual environment:

```
sudo pip3 install virtualenv
```

5.) Make virtual environment:

```
python3.7 -m venv TFLite-venv
```

6.) Activate Environment:

```
source TFLite-venv/bin/activate
```

7.) Install the dependencies:

```
bash get_py_requirements.sh
```

8.) Make sure the camera module is enabled:

```
sudo raspi-config
```

9.) Go to Interface Options and make sure the Pi Camera is enabled.

10.) Connect Pi Camera Module to Raspberry Pi.

# Running Detection

11.) After all your hardware and software is configured correctly run the following command:

```
python TFLite_detection_webcam_loop.py --modeldir=TFLite_model_bbd --output_path=processed_images
```

Where the --output_path you specify is where you want images saved.

12.) The script will start running and wait for you to press the GPIO input button to start processing the video feed from the camera.
Processed images will be saved to the '--output_path' you specified over the command line.

13.) If you like, make a video out of the images.

if you cannot install any package from the get_py_requirement.sh then just search the package on the google and install the latest version it should work.
