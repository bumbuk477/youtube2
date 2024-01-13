# youtube2
from PyQt5.QtCore import *
from PyQt5.QtWidgets import *
def winner():
    window = QMessageBox
    window.setText("Ви виграли зустріч з творцями каналу!")
    window.exec()
def looser():
    window = QMessageBox
    window.setText("Пощастить іншим разом!")
    window.exec()
app = QApplication([])
win = QWidget()
win.setWindowTitle("Конкурс від Crazy People")
win.resize(400,200)
win.move(100,100)
text = QLabel("Як звали першого ютуб-блогера, який набрав 100000000 підписників?")
rbtn1 = QRadioButton("PewDiePie")
rbtn2 = QRadioButton("Рет і Лінк")
rbtn3 = QRadioButton("SlivkiShow")
rbtn4 = QRadioButton("TheBrianMaps")
rbtn5 = QRadioButton("Mister Max")
rbtn6 = QRadioButton("EeOneGuy")
line= QVBoxLayout
line.addWidget(text,alignment=Qt.AlignCenter)
line1 = QHBoxLayout
line1.addWidget(rbtn1,alignment = Qt.AlignCenter)
line1.addWidget(rbtn2,alignment = Qt.AlignCenter)
line2= QHBoxLayout
line2.addWidget(rbtn3,alignment = Qt.AlignCenter)
line2.addWidget(rbtn4,alignment = Qt.AlignCenter)
line3 = QHBoxLayout
line3.addWidget(rbtn5,alignment = Qt.AlignCenter)
line3.addWidget(rbtn6,alignment = Qt.AlignCenter)

line.addLayout(line1)
line.addLayout(line2)
rbtn1.clicked.connect(winner)
rbtn3.clicked.connect(looser)
rbtn2.clicked.connect(looser)
rbtn4.clicked.connect(looser)
rbtn5.clicked.connect(looser)
rbtn6.clicked.connect(looser)



win.show()
app.exec()
