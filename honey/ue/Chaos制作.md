
骨骼Mesh，双击打开，工具栏上面可以看到`Make Static Mesh`的选项，可以将已有的骨骼资源导出成一个静态网格。

[十分钟快速掌握chaos破碎效果 学习视频](https://www.bilibili.com/video/BV1Hb4y1T7QE/?vd_source=8d93ec62138c112af1ea8d6ccf035cb1)

[Chaos官方基础教学](https://www.bilibili.com/video/BV1iJ4m187PF?p=1&vd_source=8d93ec62138c112af1ea8d6ccf035cb1)

Cluster即簇破碎，会根据给定的点，在点附近密集型破碎小块。

引擎中的默认资源，好像可以设置坚硬部分的框体

![[Pasted image 20240521143148.png]]

然后可以对破碎模型的属性中设置已创建的Field
![[Pasted image 20240521143344.png]]

![[Pasted image 20240521143427.png]]

可以将蓝色`MasterField`理解为破坏区，黄色`AnchorField`理解为防御区

![[Pasted image 20240521143637.png]]

破坏区调整这些属性可以改变施加力度，从而模拟（爆炸！）向外弹射碎片！

演示示例：可以在发射物撞击到物体时，获取发射物的位置，在该位置生成破坏区并调整力道等属性，然后然碰撞到的物体进行炸裂

![[Pasted image 20240521144020.png]]