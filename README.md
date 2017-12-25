# deepfakes_faceswap
This is the code from [deepfakes' faceswap project](https://www.reddit.com/user/deepfakes/).
Hope we can improve it together, HAVE FUN!

Message from deepfakes:

**Whole project with training images and trained model (~300MB):**  
anonfile.com/p7w3m0d5be/face-swap.zip or [click here to download](anonfile.com/p7w3m0d5be/face-swap.zip)

**Source code only:**  
anonfile.com/f6wbmfd2b2/face-swap-code.zip or [click here to download](anonfile.com/f6wbmfd2b2/face-swap-code.zip)

**Requirements:**

    Python 3
    Opencv 3
    Tensorflow 1.3+(?)
    Keras 2

you also need a modern GPU with CUDA support for best performance

**How to run:**

    python train.py

As you can see, the code is embarrassingly simple. I don't think it's worth the trouble to keep it secret from everyone.
I believe the community are smart enough to finish the rest of the owl.

If there is any question, welcome to discuss here.

**Some tips:**

Reuse existing models will train much faster than start from nothing.  
If there are not enough training data, start with someone looks similar, then switch the data.


Face alignment scripts based on https://github.com/1adrianb/face-alignment

Please check Phil_Latio's comment to learn how to install this repo.

After testing it's own examples/detect_landmarks_in_image.py, make sure it works.

Copy align_images.py and umeyama.py into face-alignment ( not face-alignment/face_alignment)

Run python align_images.py your_raw_image_folder

The script will create an aligned subfolder and an alignments.json file under your raw images folder.

You may remove bad aligned images in aligned folder.

Copy merge_faces.py into face-swap project folder.

Run python merge_faces.py your_raw_image_folder

The script will convert every existed aligned image with trained model, and merge it back to original raw image. The new images will be saved to merged subfolder under raw images folder.

I have tested these scripts in my environment. However if there is any issue please let me know.
