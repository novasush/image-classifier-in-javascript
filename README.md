# A cat dog image classifier deployed client side using javascript

![image](https://novasush.com/blog/images/cat_vs_dog_in_javascript.jpg)

# Instructions
1. Train a keras classifier and save its weights
2. install `tensorflowjs` python library
```bash
pip install tensorflowjs
```
3. Use tensorflowjs converter tool to convert h5 weights to js format.
```bash
tensorflowjs_converter --input_format=keras ./model.h5 ./jsweights
```
* Make sure the .h5 weights location is correct and also destination path exists.

### After running above command you will see `model.json` and `.bin` files, tensorflowjs converter dumps model architecture in `model.json` and it's weights in `.bin` files.

# setup
* Place your converted weights inside `weights` folder

* Open `classifier.js` and update `model.json` path according to your weights folder

* After everything is setup up perfectly run below command inside the directory.

```bash
python3 -m http.server
```

* navigate to [localhost](http:127.0.0.1:8000) 

# Output

![courage_garfield](https://novasush.com/blog/images/courage_garfield.jpg)
