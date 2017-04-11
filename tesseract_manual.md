# Tesseract-OCR训练使用手册


## 要求

### Windows10(不建议)

1. 启用windows10的bash功能。
1. Python2.7(Windows10Bash功能自带Python2.7)。
1. 需要将Tesseract-OCR装入bash 

### Linux

1. python2.7
1. Tesseract-OCR&ensp;3.0以上版本。
1. 将Tesseract-OCR目录加入系统路径。
1. jTessBoxEditor1.5以上

找到一个空文件夹作为工作目录。接下来的工作都会在工作目录中进行。

## 具体步骤

1. 新建一个pics目录，将需要进行训练的图片全部放在pics目录下。
1. 合并图片。运行merge.py。
1. 降噪处理。运行jiangzao.py.
1. 格式转换。将得到的result.jpg转换为tif格式。
1. 重命名图片。重命名为[lang].[fontname].exp[number].tif。
1. 获得初步boxfile。运行getBox.py&ensp;[lang].[fontname].exp[number]。
1. 查看box切分结果。使用jTessBoxEditor打开tif图片，确保目录下同时存在相应的boxfile。
1. 使用目录下的column.txt帮助检查结果。colume.txt中保存的是从左到右每一列最下面一个字符是第几个字符。(因为初步获取的boxfile容易切漏字，如果发现有切漏字的情况可以定位到具体第几个字然后手动添加boxfile条目)
1. 修改boxfile。确认切分正确后，将字典放在目录下(dict.txt)，运行changeBox.py&ensp;[lang].[fontname].exp[number]&ensp;dict
1. 训练：运行train.py&ensp;[lang].[fontname].exp[number]&ensp;[fontname]。
1. 将目录下生成的traineddata文件放入Tesseract-OCR的data目录下。
