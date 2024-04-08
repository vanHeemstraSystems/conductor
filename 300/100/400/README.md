# 400 - Standalone UI Image

From the docker directory,

```
$ docker build -t conductor:ui -f ui/Dockerfile ../
$ docker run -p 5000:5000 -d --name conductor_ui conductor:ui
```

This builds the image ```conductor:ui``` and runs it in a container named ```conductor_ui```. The UI should now be accessible at ```localhost:5000```.

**Note**<br/>
In order for the UI to do anything useful the Conductor Server must already be running on port 8080, either in a Docker container (see above), or running directly in the local JRE.
Additionally, significant parts of the UI will not be functional without Elastisearch being available. Using the docker-compose approach alleviates these considerations.
