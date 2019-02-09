# UnityKnowledge
2D游戏
可以通过代码改写相机的视野大小,函数为camera.orthographicSize=什么什么；
相机的视野大小不能直接设值，需要除以单位像素，unity默认的单位像素值为100f；
1、想先将背景等资源的position设置为0,0.然后获得背景的大小Vector2（），（其y值/2）/单位像素值。
