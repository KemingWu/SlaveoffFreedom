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
2022/7/4
QDir负责切换目录，枚举子文件夹和文件，并且可以对子文件夹、文件进行排序和过滤；
QFileInfo用于获取单个子文件夹或单个文件的详细信息
Unix/Linux系统的文件路径分隔符是'/',Windows系统的文件路径分隔符是'\'
Qt程序代码都用'/'作为文件路径分隔符
QDir既可以接受相对文件路径，也可以接受绝对文件路径。
isRelative()判断自己包含的路径是否为相对路径;isAbsolute()判断自己包含的路径是否为绝对路径
bool QDir::makeAbsolute()将路径转换为绝对路径
QString QDir::path() const //可能是相对路径，也可能是绝对路径
QString QDir::absolutePath() const //一定返回绝对路径
bool QDir::exists(const QString &name)const//参数里既可以判断文件夹，也可以判断文件的存在性
bool QDir::exists()const//不带参数，判断QDir对象自身路径是否为存在的文件夹，只管文件夹！
void QDir::setPath(const QString &path)//重新设置QDir对象的路径
QDir("Documents/Letters/Applications").dirName()   //返回 "Applications"
QDir().dirName()                                 //返回  "."
bool QDir::cd(const QString & dirName)
//比setPath()智能，常用；会自动检查参数里的目录是否存在；不存在返回false，原路径不变;切换目录成功就返回True,并进入新目录
bool QDir::caUp()//切换到父目录
bool QDir::mkdir(const QString & dirName) const    //创建新目录
bool QDir::rename(const QString & oldName, const QString & newName) //重命名旧的目录
bool QDir::rmdir(const QString & dirName) const    //只能删除一个空目录
void QDir::refresh() const //刷新缓存



























