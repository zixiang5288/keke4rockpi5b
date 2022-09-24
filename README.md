# keke4rockpi5b //**个人完全验证**//
## 给RockPi 5B V1.4硬件版本用的壳壳

![rp1](/img/rp1.jpg "图")

![rp2](/img/rp2.jpg "图")

![rp3](/img/rp3.jpg "图")

![rp4](/img/rp4.jpg "图")

![rp5](/img/rp5.jpg "图")

![上图](/img/P1.jpg "上图")

![下图](/img/P2.jpg "下图")

![风道剖视图](/img/P3.jpg "风道剖视图")

# 物料购买注意事项
1. 散热鳍片25x25x11
2.  滚花螺母尺寸M3 H4 D4.5
    滚花螺母尺寸M3 H4 D4.5
    滚花螺母尺寸M3 H4 D4.5
    重要的事情嗦三遍
3. 摄像头，屏幕，GPIO排针都需要线材引出
4. 无线网卡需要用粘上去的那种天线

# FDM注意事项（实时更新，0.4线宽，0.2层高）：
1. 下盖建议只打两层壁，不然搭桥会出现一点问题
2. 应该都不需要打支撑，有的话qq/issue见

# 关于风扇脚本
1. 需要sudo权限，要自启的话需要自行操作一下
2. 默认用的开关模式，有些烂风扇（鹏达蓝图的“静音”3010）在某个转速区间下会产生相当大的震动，高于温度墙开机，低于期望温度关闭，期望温度应当低于温度墙。
3. 需要根据风扇的情况设定 最大转速值，最小转速值，死区值 都在py开头。就不单独开个文件写了
4. 还有个比例控制，在期望温度和温度墙之间比例调节转速，这就意味着理论上讲如果需要设定风扇最小转速高于实际死区才能达到期望温度，即在低于或者接近期望温度时风扇也会保持一定转速，参考pid控制没有i的情况。但是实际情况测温还有温度传导有个延迟环节，所以系统是可能能震荡到目标值的。
