Label the Training Dataset
==========================

In this activity, you will label the training dataset images to distinguish as infected or uninfected with Pneumothorax.

<img src= "https://media.slid.es/uploads/1525749/images/10561913/Infected_Uninfected_Images.png" width = "480" height = "320">



Follow the given steps to complete this activity:

1. Label the training dataset

* Open the main.py file.

* Create path variable and store the path of the dataset folder.

    `path = "Pneumothorax-New-Dataset"`

*  Create two lists `infected` and `uninfected` to store the `infected` and `uninfected` images.

    `infected = []`

    `uninfected = []`

* Write a for loop to go through each image path in the path variable's location.

    `for img in os.listdir(path):`

* Add a `try` block.

    `try:`

* Print path of the image.

    `print(img)`
    
* Use `split` method to split the image name from `"_"` character to get the first character representing type of image and save it in type variable.

    `type = img.split("_")[0]`

* Read the image using `cv2.imread()` method and pass `path` and `img` as string to it.

    `img = cv2.imread(str(path)+"/"+str(img))`

* Covert the image from `BGR` to `RGB`.

    `img = cv2.cvtColor(img,cv2.COLOR_BGR2RGB)`

* Check if `type == 0`  and append the image in the `infected` list `else` append in the `uninfected` list.

    `if type == '0':`

        `infected.append(img)`

    `else :`

        `uninfected.append(img)`

* Add an `except` block .

    `except:`

        `print("error in reading")`


* Print length of `infected` image list.

    `print("Count of infected images", len(infected))`

* Print length of `unfected` image list.

    `print("Count of uninfected images", len(uninfected))`

* Save and run the code to check the output.
