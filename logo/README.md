## Logo

The logos are embedded bitmap images inside QR codes that contain a URL to the website.

### How to make embedded images in QR codes

* Using [GIMP](https://www.gimp.org/), create a black/white/transparent pixel graphic of the image you want to embed (`01_pixel_*.xcf`)
* Export the graphic to a gif (`02_pixel_*.gif`)
* Using [qr-vanity](https://github.com/mzollin/qr-vanity), generate QR codes for "https://vax.codes" with the image embedded in it
  * `sudo apt install git python3-dev python3-setuptools python3-pip libzbar0 libzbar-dev`
  * `virtualenv -p python3.7 venv`
  * `source venv/bin/activate`
  * `git clone https://github.com/mzollin/qr-vanity.git`
  * `cd qr-vanity`
  * `pip3 install -r requirements.txt`
  * `./qrvanity.py /path/to/pixel_vax-codes.gif "https://vax.codes"` (will generate possible QR code png images)
* Select whichever output image you think looks best (`03_output_*.png`)
* Optimize via [pngcrush.com](https://pngcrush.com) (`04_qr_*.png`)

