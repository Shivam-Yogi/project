Image Filter
============

An image operation and filter tool depends on Pillow, just for study and communication.

# Dependency
- Python3
- Numpy
- Pillow


# Usage
Show Help
```
python image_filter.py -h
```

List filters
```
python image_filter.py -l
```

Filter image
```
python image_filter.py -f grey -i images/test.jpg -o images/
```

Some filters need parameters

```
python image_filter.py -f gaussian_blur -i images/test.jpg -o images/ -a radius=3
```

Resize image (thumbnail)
```
python image_filter.py -i images/test.jpg -o out.jpg -f rgb --width=300 --height=300
```

Add water mark image
```
python image_filter.py -i images/test.jpg -o images/img_mark.jpg -f rgb -m images/water_mark.png -p RT
```

Add water mark text
```
python image_filter.py -i images/test.jpg -o images/txt_mark.jpg -f rgb -x wwtg99 --font-size=40 --font-color=100,100,100,200
```

# Filters
- rgb: RGB image
- rgba: RGBA image
- grey: Gray scale
- hand_drawn: Hand drawn
- edge_curve: Find edges
- blur: Blur
- contour: Contour
- edge_enhance: Enhance edge
    - more: More enhancement
- emboss: Emboss
- smooth: Smooth
    - more: More smooth
- sharpen: Sharpen
- gaussian_blur: Gaussian blur
    - radius: Blur radius
- min: Picks the lowest pixel value in a window with the given size
    - size: 3 or 5, default 3
- median: Picks the median pixel value in a window with the given size
    - size: 3 or 5, default 3
- max: Picks the largest pixel value in a window with the given size
    - size: 3 or 5, default 3
- mode: Picks the most frequent pixel value in a box with the given size. Pixel values that occur only once or twice are ignored; if no pixel value occurs more than twice, the original pixel value is preserved
    - size: 3 or 5, default 3
- unsharp_mask: Unsharp mask
    - radius: Blur Radius, default 2
    - percent: Unsharp strength, in percent, default 150
    - threshold: Threshold controls the minimum brightness change that will be sharpened, default 3
- emboss_45d: Emboss from 45 degree
- sharp_edge: sharp edge
- sharp_center: sharp center
- emboss_asym: Asymmetric emboss# project
