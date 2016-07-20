# Pokemon-Go-Watson
Pokemon Go With Watson Visual Recognition API

Started during AT&T Shape Hackathon 2016. Winner of Watson API Challenge.

[IBM Blog Post](https://www.ibm.com/blogs/internet-of-things/pokemon-go-watson/)

The Pokemon Go Watson Alerter periodically creates screenshots of the foreground app, classifies the image with a pre-trained Watson Visual Recognition classifier, then outputs the class names to a WebSocket endpoint.

1. Create a Bluemix account and create a Visual Recognition Service

2. Train a classifier with self-created Pokemon Go screenshots either by cloning and using the [sample trainer webapp](https://visual-recognition-demo.mybluemix.net/) or through the SDK. An example classier can have the following positive classes: haspokemon or nopokemon. You can be even more ambitious and create a classifier for each type of pokemon.

3. Update Config.java with your configs

4. (optional) Set up a WebSocket Server using [Node-RED](https://developer.ibm.com/recipes/tutorials/creating-a-nodered-application-on-bluemix/) or [AT&T Flow Designer](https://flow.att.io) and create flow using WebSocketNodeRED/flow.json.

5. Start Pokemon Go

6. Start the Pokemon Go Watson Alerter, then change the foreground app to Pokemon Go. If  ENABLE_WEBSOCKET_OUTPUT is true, client apps connected to the endpoint should start seeing output.

## Future Work
Create an android app that allows users to classify screenshots and upload the image/classification to the classifier, allowing crowdsourcing of training.

NOTE: Android classifier alert app based on fork from [https://github.com/mtsahakis/MediaProjectionDemo](https://github.com/mtsahakis/MediaProjectionDemo)
