Keras will apply many operations on its own to increasing the training set (e.g., rotate, change color, etc.).

NAIP is 1-meter per pixel.

Trained models to consider: ResNet-50, Alexnet, VGG16.

We can use 500x500 imagery.

87 sample tagged images (0 or 1) are 5000x5000 pixels.  
Idea: Downsample to smaller for first test.  
Approximately 70,000 kb per sample image.  
Approximately 30% have reservoir, 70% not reservoir.

David: Ideally, we would draw polygons around reservoirs. Then during pre-processing, script would automatically, e.g., select 500x500 rectangles surrounding all reservoirs, as well as a bunch of 500x500 rectangles which do not include reservoirs.

David (question): What is input/output of test in Alex's CNN model? That is, do we pass in 1) 500x500 rectangles, or 2) whole map? Does CNN predict 500x500 rectangles which may contain reservoir? Or ......??

Other questions: ...................

### Tasks / todos
Alex (task): Create basic CNN (with bad accuracy) to start.

Shuyu (task): Downsample 87 sample images to 500x500 for Alex to use in basic CNN ("first attempt").

Shuyu, Nitya, Ramana (task): Tag 500x500 images. (How many....?) Complete by .... this weekend?

David (task): Try tutorial "How to Segment Buildings on Drone Imagery with Fast.ai & Cloud-Native GeoData Tools" and/or further discuss with Vignesh this idea.

Shreya (task): Stay up to speed on everyone's progress? Review Google mapping API for final map of small reservoirs. For example, review here: (https://www.w3schools.com/graphics/google_maps_intro.asp). In particular, section on *markers*. Alco can review Google Maps platform here: (https://developers.google.com/maps/gmp-get-started).

Other todos:
* Final report
* Create a display of the CNNs effectiveness (i.e., a map showing TP, TN, FP, FN predictions of small reservoirs and dams).
