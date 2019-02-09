# UnityKnowledge
2D游戏
可以通过代码改写相机的视野大小,函数为camera.orthographicSize=什么什么；
相机的视野大小不能直接设值，需要除以单位像素，unity默认的单位像素值为100f；
1、设立比例值Scale：Screen.height/背景图片宽度（横屏游戏）;
2、将背景等资源的position设置为0,0.然后获得背景的大小Vector2（x,y），相机的缩小比例为（背景y值/2）/单位像素值。
