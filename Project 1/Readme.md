##Simple Deployment with Docker

*In this project I made a simple Docker deployment of a pickle file and made prediction through the exposed port.

* The predict.py has the model loaded and have  builds a endpoint using Flask api through which you can make api calls to get the predictions which has been done using the test.py

* The test.py file posts the input  json format through the exposed port and prints the result

-  In order to run the docker file first you need to build it using

```bash
docker build -t ride-duration-prediction-service:v1 .
```

- Once it has finished the build you can proceed to run it by 

```bash
docker run -it --rm -p 9696:9696  ride-duration-prediction-service:v1
```