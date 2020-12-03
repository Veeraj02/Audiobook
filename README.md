import pyttsx3
import PyPDF2
EBook = open('NAME.pdf', 'rb')
Reader = PyPDF2.PdfFileReader(EBook)
pages = Reader.numPages
print(pages)
speaker = pyttsx3.init()
for num in range(PAGENUMBER, pages):
    page = Reader.getPage(num)
    text = page.extractText()
    speaker.say(text)
    speaker.runAndWait()
