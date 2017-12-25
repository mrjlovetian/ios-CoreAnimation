# core animation  读书笔记
* 和UIView最大的不同是CALayer不处理用户交互
* CALyaer的寄宿图（即图层中包含的图）
* CALayer与UIView的contentMode对应的属性叫contentsGravity
* ContentsScale属性定义了寄宿图的像素尺寸和视图大小比例，默认情况下她是一个值为1.0的浮点数
* 把contentsGravity设置为KCAGravityCenter（这个值并不会拉伸图片）,代码方式来处理寄宿图的时候，一定要记得手动设置图层的contentsScale属性
* UIView的clipsToBounds对应CALayer的makesToBounds属性
* contentsRect，和bounds、frame不同，contentsRect不是按点来计算的，它使用了单位坐标，单位坐标指定在0到1之间，默认的contentsRect是{0，0，1，1}，可以用来裁图
*  LayerSprites是APP中使用拼合开源库
*  contentsCenter其实是一个CGRect，默认情况下contentsCenter是{0，0，1，1}，设置{0.25，0.25，0.5，0.5}，效果和UIImage里的-resizableImageWithCapInsets:非常类似
*  给contents赋值CGImage的值不是唯一设置寄宿图的方法，可以使用-drawRect：方法自定义绘制
*  UIView的frame,bounds和center对应CALayer的frame,bounds,position属性
*  archorPoint用单位坐标来描述，左上角是{0，0}，右下角是{1，1}，默认是{0.5，0.5}，用法（手表指针）


