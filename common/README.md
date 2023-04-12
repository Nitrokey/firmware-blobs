
# How to properly create a bootsplash

* create a new image in gimp with 1920x800 px 
  (more seems not to work)

* paint your picture 

* set "Image" -> "Mode" -> "Indexed"

* export this as `gimp-exported.bmp` with the following settings:
  * Run-Length Encoded
  * Compatibility options -> Do not write color space information

* now `convert` the image like that:
  ```
  convert gimp-exported.bmp -alpha off -depth 8 -compress none BMP3:my-bootsplash.bmp
  ```

* the result can be used for Tianocore/EDK2 as bootsplash


