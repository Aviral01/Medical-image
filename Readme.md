# Medical Image
Digital pathology has emerged with the digitization of patient tissue samples and in particular
the use of digital whole slide images (WSIs). Image analysis of WSIs (Whole Slide Images),
promises to play an important role in helping the pathologists by indicating potential disease
locations and by aiding their interpretation.
These images are very large therefore problem arises in analysing them as a whole. So
sometimes they are used as a whole or sometimes they are divided into tiles. However, they
cannot be analysed properly further if any pen marks are present on it. Also only the tissue
region in the slide is important. To analyse the fine details, various filters and masks are applied
on it.
Stain color from one laboratory differs from other. Even though they might be of same organ,
same tissue of two images might appear different. Segmentation is used in these images to
localize the object. However, due to very less variations in the images visually, it becomes
difficult to classify objects and localize them.

# Data Provided
Link to Data:
https://drive.google.com/drive/folders/1YOR8wBtvl1V0757qGZpNMcUc3FyB2oiI
Data is present in a folder called, assignment data.
## Inside that folder first folder is whole slide images, in which two whole slides images are
present.
1. Normal lymph node with an extension of .svs.
2. Reactive lymph node with an extension of .svs.
Any of them can be used for task 1 and 2.
## These are the following tasks that one may need to complete with python:
1. Break the Whole Slide Image into tiles or patches(must include more tissue content).
2. Perform image processing, such that resultant sample from two slides are visually same.

# Operations
Here, I use openslide to read a whole slide image. 
I will then extract a lower reolution version of the image to normalize it and then to extract H and E signals separately. 

I will also perform the exact operation on the entire whole slide image by extracting tilee, processing them, and saving processed images separately. 

Please note that this code will not cover putting tiles back into a whole slide image (image pyramid). You can explore pyvips or similar package to put together tiles into an image pyramid. 

# Openslide
OpenSlide can read virtual slides in several formats:
Aperio (.svs, .tif)
Hamamatsu (.ndpi, .vms, .vmu)
Leica (.scn)
MIRAX (.mrxs)
Philips (.tiff)
Sakura (.svslide)
Trestle (.tif)
Ventana (.bif, .tif)
Generic tiled TIFF (.tif)

OpenSlide allows reading a small amount of image data at the resolution 
closest to a desired zoom level.

pip install openslide-python

