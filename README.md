# driving_detection
some pieces

# 这是显示最基础的界面的主函数

import sys
from PyQt5.QtWidgets import QMainWindow, QApplication
from drivingSystem import Ui_MainWindow

from PyQt5.QtGui import QActionEvent

class BruceMainWindow(QMainWindow):
    """主界面类"""

    def __init__(self):
        super(BruceMainWindow, self).__init__()
        self.ui = Ui_MainWindow()  # designer画的界面
        self.ui.setupUi(self)

        #self.set_connect()  # 配置链接点
        #self.initUI()  # 原初始化的UI界面
        #self.initTimer()  # 初始化定时器



        # 以下是相关的action动作的链接！

        #self.ui.labelTips.hide()
        self.ui.pushButton.clicked.connect(self.close)
        #self.ui.action_10.clicked.connect(self.close)
        self.ui.action_10.triggered.connect(self.close)









if __name__ == "__main__":
    app = QApplication(sys.argv)
    main_window = BruceMainWindow()
    main_window.show()
    sys.exit(app.exec_())


# Links: https://rustfisher.github.io/2016/12/28/PyQt_note/PyQt-QMainWindow_simple_practice/




