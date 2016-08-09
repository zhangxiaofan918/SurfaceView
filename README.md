# SurfaceView
SurfaceView which used for play video


简单说一下以下两个属性：
setZOrderOnTop(true) 会把surafaceview置于最顶层

setZOrderMediaOverlay(true) 会把该surfaceview置于其他媒介的上面

但实际程序中遇到的场景一般用不到这两个属性，除非你的surfaceview上面没有其他控件，否则会被遮挡。
对于被遮挡的情况，我的处理方式是不使用上面的属性，而是使用addview(View v,int id)动态添加surfaceview，层次位置通过id来控制。
