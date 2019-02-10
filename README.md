# UnityKnowledge
2D游戏
可以通过代码改写相机的视野大小,函数为camera.orthographicSize=什么什么；
相机的视野大小不能直接设值，需要除以单位像素，unity默认的单位像素值为100f；
1、设立比例值Scale：Screen.height/背景图片宽度（横屏游戏）;
  竖屏游戏需要在playerSetting里设置DefaultOrientation为Portrait。Game面板里设置比例为9:16或其它。
2、将背景等资源的position设置为0,0.然后获得背景的大小Vector2（x,y），相机的缩小比例为（背景y值/2）/单位像素值100。
以下为安卓手机设置屏幕的方向：
Default Orientation意思是默认的方向
Portrait：竖屏
Portrait Upside Down：竖屏，手机倒过来
Landscape Right：横屏，屏幕在home右边
Landscape Left：横屏，屏幕在home左边（常用）
Auto Rotation：自动旋转屏幕
Auto Rotation有额外选项，可以只勾选某些方向，根据个人需求来指定旋转方向。

//以下代码写在Update()中，并乘以时间增量；
float translation=Input.GetAxis("Vertical")*MoveSpeed;//垂直的，返回（-1，1）
float rotation=Input.GetAxis("Horizontal")*RotateSpeed;//水平的，返回（-1，1）；
transform.translate(?,?,?);//将前进方向换成变量
transform.Rotate(0,0,0);//变量在哪里说明围着哪一个轴转，特别的，它是相对于父物体的坐标转

//获取鼠标移动的增量，返回的值不在（-1,1）之间
float h=Input.GetAxis("Mouse X")*Speed;
float v=Input.GetAxis("Mouse Y")*Speed;

transform.Rotate(V,h,0);




