# Face-Detection

To perform basic face detection, cropping, and blurring using OpenCV (cv2), you'll need to use a combination of image processing techniques and pre-trained models. Below is a step-by-step guide on how to achieve this

Explanation:
cv2.CascadeClassifier: Loads the pre-trained Haar cascade classifier for face detection.
cv2.cvtColor: Converts the input image to grayscale, which is required for face detection.
face_cascade.detectMultiScale: Detects faces in the grayscale image using the Haar cascade classifier.
Iterates over the detected faces, draws rectangles around them (cv2.rectangle), and crops each face region.
Applies Gaussian blur (cv2.GaussianBlur) to the cropped face region.
Replaces the original face region with the blurred face.
Displays the final image with blurred faces.
Notes:
Parameters:

scaleFactor: Parameter specifying how much the image size is reduced at each image scale.
minNeighbors: Parameter specifying how many neighbors each candidate rectangle should have to retain it.
minSize: Minimum possible object size. Objects smaller than this size will be ignored.
Customization:

Adjust the blur parameters (kernel size and sigma) for different levels of blur.
Experiment with different Haar cascade classifiers (haarcascade_frontalface_default.xml) for improved face detection in various conditions.
