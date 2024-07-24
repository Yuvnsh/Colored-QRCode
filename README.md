# Colored-QRCode
This project demonstrates how to generate a colored QR code using Python. The script utilizes the qrcode library to create a QR code and the Pillow library to manipulate its colors.


import qrcode
from PIL import Image

qr= qrcode.QRCode(
            version=1,
            error_correction=qrcode.constants.ERROR_CORRECT_H,
            box_size=10,
            border=4,
)

qr.add_data("https://www.google.com/")

qr.make(fit=True)

img=qr.make_image(fill_color="red",back_color="white")

img.save("clored_QR.png")
