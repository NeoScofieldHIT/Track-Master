# Track-Master
2017/11/09:   能够完成简单几何射线的射线追踪，没有考虑真实物理场景，没有延时损耗等  
2017/11/10：  初始版本original，这个是经过改进之后的原始版本，结构更清晰，同样没有考虑延时等  
2017/11/13：  之前的版本中存在反射次数不足就停止反射的情况（舍入误差问题），当前版本对存在的问题进行了修复  
2017/11/15：  delta=0.05，发射点坐标（250,400），射线编号为nls=4501时，刚好射到墙角，程序出现维度问题（射线追踪的固有弊端）。除此之外，Recv的接收值为空的问题已解决  
2017/11/16：  得到了功率的分布图，但是应该存在问题，比如平行于坐标轴的功率值较低的直线等，这些需要解决的问题
2017/11/17：  得到了功率分布图和多径分布，感觉多径不太明显。修复了之前的一些问题，现在程序基本没有大的问题
2017/11/22：  之前的仿真结果中没有看出明显的多径衰减，主要是因为采样点的半径设置过大，导致接收径信息过多造成的，对其进行了更正，ErrMar=0.15cm
2017/11/29：  目前针对场分布的工作已经基本完成，接下来开始多径信号合成的部分。场分布存盘（画场分布的程序origin.zip）
2017/12/01：  当前针对基于LFM-FRFT的信号参数检测已经能够实现，存在的问题是一致采样的问题。参数检测存盘（LFM信号参数估计origin.zip）