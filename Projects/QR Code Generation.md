```py
import qrcode

# Transfering txt file into QR Code
text = input("Enter your text: ")
name = input("Enter the name of QR Code: ")

txt = qrcode.make(f"{text}")                      #Creates QR Code with the text you have given
txt.save(f"{name}.png")                           #Save QR Code with the name you have given


#Transfering Photo file into QR Code          #(NOT FINISHED YET)
...


#Tranfering GIF file into QR Code             #(NOT FINISHED YET)
...


#Tranfering Video file into QR Code           #(NOT FINISHED YET)
... 


#Creating URL with QR Code
flop = input("Enter the name of QR Code: ")                    # Name of QR Code
url = input("Enter your url (site name): ")                    # URL
qr = qrcode.QRCode(version=1,
                   error_correcttion=qrcode.constant.ERROR_CORRECT_L,
                   box_size = 20,
                   border = 2)                             #Adding factors to QR Code

qr.add_data(f"{url}")
img = qr.make_image(fill_color = "black", back_color = "white")   # here you can change colors of QR Code if you want  to
img.save(f"{flop}")
```
