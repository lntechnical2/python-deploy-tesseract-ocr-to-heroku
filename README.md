deploy Tesseract-OCR to Heroku(Linebot)
==== 

Descript
-------

Because I have stuck on the this question for two days,I take some notes to remind me of deeploying the Tesseract-OCR to Heroku.First, Tesseract is an OCR sponsored by Google. It is open-source and its binaries are available for lots of platforms, Additionally, it is a popular go-to library when OCR functionalities are required in an app. Setting up Tesseract-OCR is a procedure in popular development environments such as Heroku.Most of all,the following article is the process of deploying and coding.

Python Code
-------

```python
import pytesseract
from PIL import Image
pytesseract.pytesseract.tesseract_cmd = '/app/.apt/usr/bin/tesseract'
image = Image.open(path)
t = pytesseract.image_to_string(image)
line_bot_api.reply_message(event.reply_token,TextSendMessage(text=t))
```

Focus on the path!!!->'/app/.apt/usr/bin/tesseract'
-------

#step













