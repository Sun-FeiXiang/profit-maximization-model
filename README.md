# profit-maximization-model
Profit Maximization for Viral Marketing in Online Social Networks
在线社交网络中的病毒式营销的利润最大化问题
模型实现
  独立级联模型（Independent cascade model）
    1.将图用邻接矩阵存储。
    2.随机生成p_vw:v激活w和w激活v的概率设置一样（测试数据中用有向边实际存储了一个无向图）。
    3.激活的节点尝试（随机生成一个激活概率）激活它的孩子，并且只能尝试激活一次（无论是否激活成功）。
    4.重复激活过程，直到不再有新的节点被激活。
  线性阈值模型（Linear threshold model）
    1.将图用邻接矩阵存储。
    2.随机生成节点阈值，随机生成节点影响力。均为[0,1]。
    3.未激活节点检测周围已激活节点，已激活节点施加影响力
    （每个激活节点施加的影响力为其自身影响力÷邻居个数）给该节点，大于其阈值则该节点被激活。

注意：模型实现基于节点是连续的；每次
