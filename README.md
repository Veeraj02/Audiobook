import pyttsx3
import PyPDF2
E-Book = open('NAME.pdf', 'rb')
Reader = PyPDF2.PdfFileReader(E-Book)
pages = Reader.numPages
print(pages)
speaker = pyttsx3.init()
for num in range(PAGENUMBER, pages):
    page = Reader.getPage(num)
    text = page.extractText()
    speaker.say(text)
    speaker.runAndWait()
