# Tilt Series data

## Data Information

- Shape: (n,w,h) n - number of slices, w - width, h - height
- Data Type: uint16
- Data Range: 0 - 37647
- Data mean: 892.5
- Data std:  328.6

## Ideal Solution

- Find structures and give unique ids.
- Average over all structures to get a single high resolution image.

# Ideas to explore

- Any linear algebra that can classify blocks of data as being similar?

# Ideas for Visualization

- Log scaling worked or resizing the image to be smaller.

# Problems

We have a lot of data. We need to find a way to reduce the amount of data we have to process.
- resizing
- reducing the number of slices

If I am correct, as each image is taken and the sample is rotated, the sample is translated. This means that the sample is not in the same position for each image. So the label only truly applies to the center image. This means that we need to find a way to align the images. Is this done in the reconstruction? I don't think so.

Cant find any bounding box information. Maybe we implement classical methods to simplify some of our problems.