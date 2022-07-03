- 👋 Hi, I’m @SlaveoffFreedom
- 👀 I’m interested in ...
- 🌱 I’m currently learning ...
- 💞️ I’m looking to collaborate on ...
- 📫 How to reach me ...

<!---
SlaveoffFreedom/SlaveoffFreedom is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
//Qt笔记//
tr("")//代表可翻译字符串的意思,封装字符串
objectName 对象名称全是指针变量名
geometry(x,y,width,height)
UI直接使用法：
QWidget *hw = new QWidget();//先创建一个对象（指针）
Ui::Form createUi; //定义Ui::Form类的对象createUi(普通变量)
createUi.setupUi(hw)//该函数接收一个窗体对象指针，为hw创建内部的控件
setStyleSheet //设置窗口或控件的显示风格，所有窗口和控件可用
setStyleSheet(tr("color : xx ; background-color : rgb(0,255,255)"))
//遇到构建问题的两种解决方法
1、修改了pro文件后，需要手动重新构建项目；2删除构建目录如build-testbug，点击构建或运行按钮，实现重新构建项目。
