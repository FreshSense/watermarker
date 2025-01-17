# watermarker
Simple CLI tool to watermark and overlay images. Built using Go.

## Special Thanks
Watermarker was built using the following wonderful packages:

[Cobra from @spf13](https://github.com/spf13/cobra)

[Imaging from @disintegration](https://github.com/disintegration/imaging)

## Install

```shell
go get -u github.com/YoungMetroTrusted/watermarker
```

## Useage
### Get help
```shell
watermarker help
```
```shell
watermarker image -h
```
```shell
watermarker bulk -h
```

### Watermark a single image
Note: This will overwrite the original image
```shell
watermarker image examples/example_image.jpg example_watermark.png
```

### Watermark a single image with custom opacity
```shell
watermarker image examples/example_image.jpg example_watermark.png -o 0.35
```

### Watermark a single image with custom opacity and write to a new file
```shell
watermarker image examples/example_image.jpg example_watermark.png -o 0.35 -n new_image.jpg
```

### Watermark all images in a folder
Note: New images will be saved to a folder named "watermarked" in the current directory
```shell
watermarker bulk imageFolder/ example_watermark.png
```

### Watermark all images in a folder with custom opacity
```shell
watermarker bulk imageFolder/ example_watermark.png -o 0.8
```

### Watermark all images in a folder with custom opacity and custom output folder
```shell
watermarker bulk C:\Users\Valb9\Downloads\concert\ watermark2.png -o 0.8 -n C:\Users\Valb9\Downloads\concert_output\
watermarker bulk imageFolder/ example_watermark.png -o 0.8 -n examples/output/bulk/
```
