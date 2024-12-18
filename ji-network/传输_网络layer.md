# 4.1.7 答案与解析  

# 一、单项选择题  

01.C
- 网络层目的
  - 选项A、B不是网络层目的
  - IP提供的是不可靠服务,因此D错误

02.C
- 网络异构性
  - 包含以下特点
    - 传输介质
    - 数据编码方式
    - 链路控制协议
    - 数据单元格式和转发机制
  - 这些特点分别在物理层和数据链路层协议中定义

03.D
- 拥塞现象
  - 定义
    - 到达通信子网中某部分的分组数量过多
    - 该部分网络来不及处理
    - 导致网络性能下降
    - 严重时可能导致网络死锁
  - 错误选项分析
    - A选项:网络性能是提高的
    - B、C选项:接收发出分组多少与吞吐量不成正比,无法判断拥塞

04.C
- 路由器特点
  - 是第三层设备
  - 向上层隐藏下层实现
  - 物理层、数据链路层、网络层协议可以不同
  - 网络层以上协议必须相同
- 常见误区
  - 误认为网络层协议必须相同
  - IPv4与IPv6网络互连是网络层协议不同的例子

05.C
- 网络设备功能比较
  - 路由器(网络层)
    - 能分隔广播域
    - 不转发广播包
    - 抑制网络风暴
  - 交换机(数据链路层)
    - 能分隔冲突域
    - 不能分隔广播域
  - 集线器和中继器(物理层)
    - 不能分隔广播域
    - 不能分隔冲突域

06.C
- 路由表特点
  - 维护目的
    - 决定分组转发
    - 提高查询效率
    - 减少维护内容
  - 包含内容
    - 目的网络
    - 下一跳路由器IP地址
  - 不保留整个传输路径信息

07.C
- 路由器工作原理
  - 是网络层设备
  - 通过IP地址标识主机
  - 根据IP地址转发分组

08.A
- 路由器转发过程
  - 接收整个分组
  - 进行错误检查
  - 存储正确分组
  - 根据路由选择协议转发
  - 采用存储转发机制

09.B
- 路由选择特点
  - 路由器仅知道下一跳地址
  - 主机只知道本地网络路径
  - 源主机只将分组发给网关
  - 均不知道完整路径

10.D
- 协议层次划分
  - 网络层协议:IP、ICMP
  - 传输层协议:TCP
  - 应用层协议:FTP

11.B
- 报文交换特点
  - 交换单元是报文
  - 报文大小不固定
  - 需要较大存储空间
  - 处理时间长且不固定
  - 不适合实时通信

12.D
- 交换方式比较
  - 电路交换:无差错控制能力
  - 分组交换
    - 有最大长度限制
    - 可分割发送
    - 数据报方式更适合出错率高的系统

13.C
- 虚电路与数据报比较
  - 虚电路
    - 有连接服务
    - 按同一路由转发
    - 保证有序到达
  - 数据报
    - 独立选择路由
    - 不保证可靠性
    - 不保证按序到达

14.D
- 分组交换方式
  - 虚电路:同一路由转发
  - 数据报
    - 独立选择路由
    - 不保证可靠性和顺序

15.D
- 参考表4.1比较虚电路和数据报

16.D
- 虚电路特点
  - 可采用存储转发
  - 包括PVC和SVC
  - 数据报无连接且不保证可靠性
  - 分组携带虚电路标识

17.C
- 虚电路服务特点
  - 提供可靠通信
  - 仅建立连接时需完整地址
  - 后续分组携带虚电路编号
  - 多站点使用不会冲突

18.C
- 虚电路工作机制
  - 建立逻辑连接
  - 故障需重新建立连接
  - 固定路径传输
  - 仅建立连接时需目的地址

19.C
- 交换技术比较
  - 电路交换和报文交换非分组技术
  - 数据报无差错控制和流量控制
  - 虚电路提供可靠有序服务

20.D
- SDN特点
  - Openflow是控制和数据平面接口
  - 路由器间不交换路由信息
  - 由远程控制器计算最佳路由

21.A
- SDN架构特点
  - 新型网络体系结构
  - 使用OpenFlow交换机
  - 使用流表替代转发表
  - 远程控制器不在交换机中

22.B
- 虚电路通信特点
  - 建立阶段需完整地址
  - 后续使用虚电路号
  - 保证有序传输
  - 无需预分配带宽

23.B
- SDN接口
  - 北向接口:面向上层开发者
  - 南向接口:控制平面与数据平面通信
  - 流表下发使用南向接口





# 4.2.9 答案与解析  

# 一、单项选择题  

01. C
- TCP和UDP是传输层协议
- IP、ICMP、ARP、RARP是网络层协议

02.B
- 协议字段
  - 值为6表示TCP
  - 值为17表示UDP
- 版本字段
  - 值为4表示IPv4
  - 值为6表示IPv6

03.C
- IP分组首部长度相关标记
  - 首部长度：基本单位为4B
  - 总长度：基本单位为1B
  - 片偏移：基本单位为8B
- 首部长度特点
  - 必须是4B的整数倍
  - 取值范围为 $5\sim15$ (默认值是5)
  - 由于可变性必不可少
- 总长度字段
  - 包括分组首部和数据部分长度
  - 单位是字节
  - 数据部分长度可由总长度减去首部长度计算

04.B
- 检验和特点
  - 只检查数据报的首部
  - 不包括数据部分
- 检验和计算方法
  - 首部划分为16比特序列
  - 用反码算术运算相加
  - 将和的反码写入检验和字段
- 检验和错误处理
  - 接收方发现错误则丢弃数据报
  - 不发送差错报文
- 检验和计算不需要伪首部
  - 伪首部用于UDP或TCP检验和

05.D
- MAC地址用途
  - 标识主机或路由器
  - 数据报到达目的网络后需要MAC地址
  - IP地址需转换为对应MAC地址

06.D
- 数据报分片传输特点
  - 每个分片独立传输
  - 可能经过不同路径
  - 在目的端主机重组

07.A
- IP首部字段用途
  - 标识字段：确认分片归属
  - 标志字段
    - DF表示是否允许分片
    - MIF表示是否还有分片
  - 片偏移：指示分片相对位置

08.D
- 片偏移特点
  - 以8B为单位
  - 标识分片在原分组中的相对位置

09.D
- 片偏移详细说明
  - 以8B为偏移单位
  - 值为0表示第1片或未分片
  - 值为100表示该片第1字节是原数据报第800字节

10.B
- 分组长度超过MTU处理
  - DF=1时
    - 丢弃分组
    - 用ICMP向源主机报告差错
  - DF=0时
    - 进行分片
    - MF=1表示后面还有分片

11.C
- 长度单位说明
  - 片偏移：8B
  - 首部长度：4B
  - 总长度：1B
- 数据计算
  - 片偏移100对应第800字节
  - 总长度100B
  - 首部长度 $4B×5=20B$
  - 数据部分长度80B
  - 最后字节编号879

12.B
- IP地址匹配分析
  - 132.19.237.5与132.0.0.0/8前8位匹配
  - 132.19.237.5与132.0.0.0/11前11位匹配
  - 132.19.237.5与132.19.232.0/22前22位不匹配
- 路由选择
  - 根据最长前缀匹配原则选择R2
  - 默认路由仅在其他都不匹配时使用
13.A
- C类IP地址特点
  - 前24位为网络位
  - 后8位为主机位
  - 主机位全"0"表示网络号
  - 主机位全"1"表示广播地址
  - 最多可有 $2^8-2=254$ 台主机/路由器

14.A
- CIDR地址块86.32.0.0/12分析
  - 网络前缀12位
  - 第2字节前4位在前缀中
  - 32的二进制为00100000
  - 4个地址前8位相同
  - 第2字节前4位分别为0010,0100,0100,0100

15.A
- 广播地址和多播地址分析
  - 10.255.255.255
    - A类地址
    - 主机号全1
    - 为网络广播地址
  - 192.168.24.59/30
    - CIDR地址
    - 后2位为主机号
    - 59二进制为00111011
    - 主机号全1为广播地址
  - 224.105.5.211为D类多播地址

16.D
- 127.xx.yy.zz地址特点
  - 为保留地址
  - 用于回路测试

17.B
- IP地址有效性分析
  - A为C类地址
    - 掩码255.255.255.0
    - 主机号全0不可用
  - C为回环测试保留地址
  - D语法错误(256非法)
  - B为有效A类地址
    - 网络号110
    - 主机号47.10.0

18.C
- 主机数量计算
  - $240_{10}=11110000_2$
  - 12位用于主机地址
  - 主机位全0和全1不可用
  - 最多主机数 $2^{12}-2=4094$

19.A
- IP数据报传输特点
  - 可能经过多个网络和路由器
  - 源IP地址和目的IP地址不变
  - 分片时地址复制到每个分片首部

20.C
- 划分子网的影响
  - 增加子网数量
  - 需要路由器连接子网
  - 减少广播域大小
  - 提高网络效率和安全性
  - 减少总主机数
  - 提高IP地址利用率

21.A
- 子网划分分析
  - 主机号有5位
  - 最少2位表示主机号
  - 剩3位表示子网号
  - 最多可分8个子网
  - 每个子网最多30个有效IP地址
22.C
- IP地址与网络关系
  - 一台主机可以有多个IP地址
  - 多个IP地址意味着属于多个网络
  - 192.168.11.25为C类地址
  - 与A、B、D属于同一网络,仅C的网络号不同

23.A
- CIDR的作用
  - 更合理分配IP地址空间
  - 缓解IP地址消耗速度
  - 通过路由聚合减少路由表数目
  - 提高网络性能
  - 不能彻底解决IP地址耗尽问题

24.D
- CIDR表示法
  - 用斜线"/"后加网络前缀位数表示IP地址
  - 网络前缀为网络号部分
  - 剩余位数为主机号部分
  - 地址块包含地址数为 $2^{10}=1024$
  - 126.166.66.99/22所在地址块第一个地址为126.166.64.0

25.B
- 默认网关设置
  - 200.15.10.7二进制最后字节为00000111
  - 是200.15.10.6/29地址块的广播地址
  - 广播地址不能作为默认网关
  - 会导致无法识别网关
  - 分组会被分发给本网络所有主机

26.D、A
- CIDR地址块特点
  - 由网络前缀和主机号组成
  - 相同网络前缀的连续IP地址构成地址块
  - 192.168.0.0/20地址块:
    - 网络前缀20位,主机号12位
    - 地址数为 $2^{12}$ 个
    - 最小地址192.168.0.0
    - 最大地址192.168.15.255
  - 192.16.0.19/28子网:
    - 子网掩码255.255.255.240
    - 192.16.0.17与192.16.0.19前28位相同
    - 192.16.0.17是该子网的主机地址

27.B
- TTL机制
  - 为每个IP分组设定生存时间
  - 每过一个路由器TTL减1
  - TTL为0时不再转发
  - 避免分组无限循环

28.D
- IP地址管理方案演进
  - 分类IP地址问题:
    - 每类地址可连接主机数过大
    - 造成IP地址浪费
  - 划分子网:
    - 借用主机号部分作为子网号
    - 将大网络细分为小网络
    - 提高IP地址利用率
  - CIDR优势:
    - 更灵活的地址分配
    - 消除传统分类地址概念
    - 使用不同长度网络前缀
    - 按需分配地址块
  - NAT技术:
    - 允许专用网络连接互联网
    - 内部可使用专用地址
    - 节省公网IP地址
  - IPv6解决方案:
    - 使用128位地址空间
    - 根本解决地址耗尽问题

29.B
- IP分片机制
  - 分片条件:
    - 分组大于网络MTU时需要分片
  - 分片特点:
    - 可独立通过不同路径
    - 传输过程中可能继续分片
    - 中间路由器不能重组
    - 只在目的主机重组
    - 到达顺序可能不同
  - 接收要求:
    - 目的主机必须支持重组能力

30.C
- 子网分配规则
  - "/29"表示前29位为网络号
  - 已分配子网74.178.247.96/29
  - 第4字节前5位为01100
  - C选项网络前缀与已分配重叠
  - 不能再分配给其他子网
31.D
- IP地址与子网掩码分析
  - 要求找到使A、B的IP地址与掩码"与"运算结果相同的掩码
  - D选项与A、B相"与"的结果均为216.0.0.0

32.B
- B类地址子网划分
  - 原始状态
    - 16位作为主机位
  - 划分需求
    - 需要51个子网
    - $2^5 < 51 < 2^6$
  - 解决方案
    - 划出6位作为子网号
    - 剩余10位用于主机号
    - 可容纳主机数为$2^{10}-2=1022$
  - 子网掩码
    - 结果为255.255.252.0

33.A
- 路由聚合分析
  - 4条路由特点
    - 前24位为网络前缀
    - 前2字节相同
  - 第3字节比较
    - 129 = 10000001
    - 130 = 10000010
    - 132 = 10000100
    - 133 = 10000101
  - 聚合结果
    - 前5位完全相同
    - 掩码1的数量为8+8+5=21
    - 聚合后网络为172.18.128.0/21

34.B
- 地址块聚合分析
  - 选项A
    - 地址块在172.16.166.192/26内
    - 存在重叠
  - 选项B
    - 与172.16.166.192/26不重叠
    - 聚合为172.16.166.128/25
    - 无多余地址
  - 选项C、D
    - 与172.16.166.192/26不重叠
    - 聚合为172.16.166.0/24
    - 引入多余地址

35.A
- 点对点链路IP地址需求
  - 需要4种组合
    - 两个主机IP地址
    - 一个网络地址
    - 一个广播地址
  - 主机号需求
    - 只需2位
  - 子网掩码
    - 255.255.255.252
    - CIDR表示为"/30"

36.B
- 子网通信问题分析
  - 子网掩码255.255.255.224
    - 前27位为网络号
  - 子网划分
    - B选项属于202.3.1.64/27
    - 其他选项属于202.3.1.32/27
  - 地址范围分析
    - 后5位为主机号
    - 三个子网地址范围:$202.3.1.1\sim30,33\sim62,65\sim94$
    - 排除全0或全1
37.D
- IP地址分析
  - 子网掩码:255.255.192.0
    - 网络号:18位
    - 主机号:14位
  - 广播地址计算
    - 基于166.66.66.66
    - 后14位置1
    - 结果:166.66.127.255

38.C
- 地址块分析
  - 类似哈夫曼编码思想
  - 用32层满二叉树表示IP地址空间
  - 每个分支节点表示地址块
  - 叶节点表示IP地址
- 子网聚合要求
  - 4个子网地址空间不重叠
  - 能构成一个新地址空间
- 选项分析
  - A、D和110/27可聚合成/24
  - B、00/26、11/26可聚合成/24
  - C需要5个子网,不符合要求

![](https://cdn-mineru.openxlab.org.cn/model-mineru/prod/ea20ba71cc1b6b61197d982c901e83ea64789e02e3a951eb2b126e7487a705cd.jpg)

39.A
- IP数据报特点
  - 首部包含源IP和目的IP
  - 路由只根据目的IP选路
  - IP地址经路由不变
- ARP广播特点
  - 只在子网内传播
  - 不同子网间不能直接ARP
- 硬件地址特点
  - 只具有本地意义
  - 每过路由需重新封装

> attention：
路由器接收到分组后,剥离该分组的数据链路层协议头,然后在分组被转发之前,给分组加上一个新的链路层协议头。

40.A
- 受限广播地址255.255.255.255
  - 仅用于主机配置
  - 路由器不转发
  - 只在本地网络中

41.C
- NAT内部地址段
  - A类:10.0.0.0~10.255.255.255
  - B类:172.16.0.0~172.31.255.255(16个B类网段,主机数1048576)
  - C类:192.168.0.0~192.168.255.255(256个C类网段,主机数65536)
- C选项为内部地址,不允许出现在公网

42.C
- ARP地址解析过程
  - 查询本地ARP缓存
    - 有映射:直接使用MAC地址
    - 无映射:广播ARP请求
  - 目的主机位置
    - 本局域网:直接发送
    - 其他网络:发送给路由器

43.C、A
- ARP请求/应答特点
  - 请求:必须广播(不知目标位置)
  - 应答:使用单播(包含发送方MAC)

44.B
- ARP请求次数计算
  - 主机A发起1次
  - 5个路由器各1次
  - 总计6次ARP请求

45.B
- 目的MAC地址确定
  - 判断是否同一子网
    - 计算网络前缀
    - 甲:211.71.128.0/20
    - 乙:211.71.128.0/20
  - 同一子网:使用乙的MAC
  - 不同子网:使用网关MAC

46.C
- DHCP特点
  - 自动获取IP配置
  - 无需手工干预

47.D
- TTL为1的IP数据报处理
  - 路由器先将TTL减1
  - 若为0则
    - 丢弃该数据报
    - 发送ICMP时间超过报文

48.A
- ICMP协议特点
  - 属于网络层协议
  - 封装在IP数据报中发送
  - 不是高层协议

49.C
- PING命令
  - 使用ICMP询问报文
    - 包含回送请求和回答报文

50.B
- IP地址分析
  - 网络地址:192.168.5.0/24
    - 网络号:前24位
    - 后8位:子网号+主机号
  - 子网划分
    - 子网掩码:255.255.255.248
    - 前5位用于子网号:可表示32个子网
    - 后3位用于主机号:可表示6台主机

51.C
- ICMP差错报告报文类型
  - 终点不可达
  - 源点抑制
  - 时间超过
  - 参数问题
  - 改变路由

52.C
- 网络地址分析
  - 地址范围:192.168.4.0~192.168.4.3
  - 主机号占2位
  - 可容纳主机数:4-2=2台

53.D
- 路由聚合
  - 子网分析
    - 192.168.2.0/25
    - 192.168.2.128/25
  - 聚合结果
    - 网络地址:192.168.2.0/24
    - 子网掩码:255.255.255.0
    - 下一跳:192.168.1.2

54.D
- 广播地址计算
  - 子网掩码第3字节:11111100
    - 前22位为子网号
    - 后10位为主机号
  - 广播地址:180.80.79.255

55.A
- ARP协议功能
  - 将IP地址解析为MAC地址
  - 用于数据链路层实际传送

56.B
- 协议层次关系
  - ICMP封装在IP分组中
  - UDP/TCP为应用层提供服务
  - PPP为网络层提供服务

57.C
- 路由选择原则
  - 最长前缀匹配
  - 169.96.40.5与169.96.40.0前27位匹配最长

58.C
- 网络通信分析
  - H1和H2在同一网络
  - H3和H4在同一网络
  - 跨网络通信需要正确配置默认网关
  - 默认网关配置错误导致通信问题

59.D
- NAT地址转换
  - 内网用户访问公网
  - 路由器接口地址分析
  - IP地址转换过程

60.C
- 子网划分计算
  - 16位主机号
  - 分成128个子网
    - 7位子网号
    - 9位主机号
  - 最大可分配IP地址数:510

61.A
- 特殊IP地址
  - 0.0.0.0/32:本机源地址
  - 127.0.0.1:回送地址
  - 200.10.10.3:C类地址
  - 255.255.255.255:广播地址

62.C
- 路由聚合分析
  - 前16位相同
  - 第3段分析
    ![](https://cdn-mineru.openxlab.org.cn/model-mineru/prod/3d12378d84831f773ecbe2d6c1336c0335596f76d06dcccde7b86ac47d8ad3c6.jpg)
  - 聚合结果:35.230.32.0/19

63.D
- MAC地址变化分析
  - 数据传递过程
    - H1到路由器R
    - 路由器R到H2
  - MAC地址变化规则

64.B
- 变长子网划分
  - 网络前缀20位
  - 5个子网划分方案
  - 最小子网可分配地址数:254

65.B
- 子网划分验证
  ![](https://cdn-mineru.openxlab.org.cn/model-mineru/prod/1204f11ecf848ccd6a04d22a4e76dac74775093d20c47d81fb54a577486e1225.jpg)
  - 互不重叠原则
  - 地址空间完整性

66.B
- IP分片计算
  - MTU=800B
  - IP首部20B
  - 分片规则分析

67.B
- 网络地址计算
  - IP地址与子网掩码按位与
  - 结果:183.80.64.0

68.D
- 默认网关配置
  - 网关地址:192.168.1.62
  - 子网掩码:255.255.255.224

69.A
- NAT地址转换过程
  - 私有地址:192.168.0.3
  - 全球地址:195.123.0.33

70.B
- 网络地址计算
  - 网络号20位
  - 地址范围分析
  - 可分配IP地址数计算

# 二、综合应用题  

01.【解答】
- IP分组首部长度和数据长度计算
  - 首部长度字段单位为4B
    - 101(二进制)=5(十进制)
    - 首部长度=5×4=20B
  - 总长度字段单位为字节
    - 101000(二进制)=40(十进制)
  - 分组数据长度=40-20=20B

02.【解答】
- IP分片计算
  - 原始数据报
    - 总长度=4000B
    - 有效载荷=4000-20=3980B
  - 分片计算
    - 最大有效载荷=1500-20=1480B
    - 分为3个片段
      - 片1: 1480B, 偏移=0, MF=1
      - 片2: 1480B, 偏移=185, MF=1  
      - 片3: 1020B, 偏移=370, MF=0

03.【解答】
- MTU限制下的IP分片过程
  - 第一次分片(MTU=1500B)
    - 片1: 数据长度1480B
    - 片2: 数据长度520B
  - 第二次分片(MTU=576B) 
    - 片1分为3个小片:
      - 552B
      - 552B
      - 376B
    - 片2保持不变:520B
  - 最终4个分片

04.【解答】
- IP分片偏移计算
  - 片偏移值=100(单位:8B)
    - 数据部分首字节编号=800
  - 分组总长度=100B
    - 首部长度=20B
    - 数据长度=80B
  - 数据部分末字节编号=879

05.【解答】
- 子网地址计算
  - 目的地址:201.230.34.0
  - 子网掩码:255.255.240.0
  - 计算过程
    - 前两部分保持:201.230
    - 第三部分按位与:32
    - 最后部分置0
  - 子网地址:201.230.32.0

06.【解答】
- CIDR路由聚合
  - 原地址块
    - 212.56.132.0/24
    - 212.56.133.0/24
    - 212.56.134.0/24
    - 212.56.135.0/24
  - 分析共同前缀
    - 前两字节相同
    - 第三字节前6位相同
    - 共同前缀长度=22位
  - 聚合结果:212.56.132.0/22

07.【解答】
- 公司网络子网划分
  - 划分要求
    - 5个部门子网
    - 每个子网20~30主机
  - 子网划分方案
    - 子网号3位(最多8个子网)
    - 主机号5位(最多30个地址)
    - 子网掩码:255.255.255.224

![](https://cdn-mineru.openxlab.org.cn/model-mineru/prod/de60a2f2ea4d9b3efa1bfb7664521f9a68fbb765626545838f0ce350db9b47f0.jpg)

08.【解答】
- 路由表匹配分析
  - 分组A匹配分析
    - 与131.128.56.0/24不匹配
    - 与131.128.55.32/28匹配28位
    - 与131.128.55.32/30匹配30位
    - 与131.128.0.0/16匹配16位
  - 路由表更新建议
    - 增加特定主机路由
    - 增加默认路由
  - 子网划分方案
    - 划分4个子网
    - 子网掩码:255.255.255.192

![](https://cdn-mineru.openxlab.org.cn/model-mineru/prod/b80eaaf41623c147e243bb933903181f30541733dd1bd4662892a0998354f177.jpg)

09.【解答】
- 路由匹配分析
  - C4.5E.10.0/20匹配
    - 目标地址C4.5E.13.87
    - 匹配20位,下一跳B
  - C4.50.0.0/12匹配
    - 目标地址C4.5E.22.09
    - 匹配12位,下一跳A
  - 80.0.0.0/1匹配
    - 目标地址C3.41.80.02
    - 匹配1位,下一跳E
  - 40.0.0.0/2匹配
    - 目标地址5E.43.91.12
    - 匹配2位,下一跳F

10.【解答】
- 自治系统IP地址分配
  - LAN3(150主机)
    - 需8位主机号
    - 分配30.138.118.0/24
  - LAN2(91主机)
    - 需7位主机号
    - 分配30.138.119.0/25
  - LAN5(15主机)
    - 需5位主机号
    - 分配30.138.119.192/27
  - LAN1(3路由器+网关)
    - 需3位主机号
    - 分配30.138.119.232/29
  - LAN4(3主机)
    - 需3位主机号
    - 分配30.138.119.240/29

11.【解答】
- 网段划分分析
  - 子网掩码255.255.255.240
  - 主机分组
    - A独立一个网段
    - B、C一个网段
    - D、E一个网段
  - IP地址范围计算
    - F所在网段:192.168.75.17~30
  - 广播地址分析
    - 广播地址:192.168.75.175
    - D、E可接收

12.【解答】
- IP首部字段解析
  - 地址字段
    - 源IP:124.78.3.2
    - 目的IP:180.14.15.2
  - 长度字段
    - 总长度:84字节
    - 首部长度:20字节
    - 数据长度:64字节
  - 分片字段
    - 片偏移:6224×8字节
    - DF=1(不可分片)
    - MF=0(无后续分片)

13.【解答】
- 网络通信分析
  - MAC地址识别
    - 目的MAC:00:1d:72:98:1dfc
    - 源MAC:00:00:5e:00:01:01
  - IP分组数据量
    - 首部长度:20B
    - 总长度:400B
    - 数据长度:380B
  - 分片处理
    - MTU=380B小于分组长度
    - DF=1不允许分片
    - 处理:丢弃并发送ICMP报文

14.【解答】
- 网络配置分析
  - R1接口IP地址和默认网关
    - R1接口E2的IP地址: 172.16.16.18/30
    - H1默认网关: 192.168.0.126 (R1接口E0)
    - H4默认网关: 192.168.0.254 (R1接口E1)
  
  - R2路由聚合
    - R1接口E0和E1直连网络聚合为192.168.0.0/24
    ![](https://cdn-mineru.openxlab.org.cn/model-mineru/prod/aff6911c55539d03b6a213f88112780e608565d3cdacf4365a1220e22bd15f59.jpg)

  - H1到H6通信过程
    - ARP使用两次
    - 交换机自学习
    - Hub广播特性分析
      - H1发送IP分组P: H4、H5、H6收到,H6接收
      - H6发送IP分组A: H4、H5、H1收到,H1接收

  - NAT服务配置
    - H1发出时
      - 源IP: 192.168.0.11
      - 目的IP: 218.75.230.30
    - R2转发时
      - 源IP: 211.67.222.16
      - 目的IP: 218.75.230.30

15.【解答】
- IP地址划分
  - 子网划分要求
    - 子网号可全0或全1
    - 主机号不能全0或全1
    - 需要2个子网
    - 每个局域网≥120个地址
  - 划分结果
    - 子网1: 202.118.1.0/25
    - 子网2: 202.118.1.128/25

- 路由表配置
  - R1路由表设置
    - 直连网络路由
    - 域名服务器特定主机路由
    - 默认路由配置
    ![](https://cdn-mineru.openxlab.org.cn/model-mineru/prod/6d8e12b92696d1caf46815042e7fe9b6e3ce3df46a9e58165ce744be9b455941.jpg)
    ![](https://cdn-mineru.openxlab.org.cn/model-mineru/prod/6946ebdea841b086720f7c0856bee515b59904783934ca57fd736bd1e6d27fff.jpg)

- R2路由聚合
  - 聚合后路由表项
    ![](https://cdn-mineru.openxlab.org.cn/model-mineru/prod/1a6d50249b6e55ffab696f63a97d92a4a95040385a86cacddb95f89b459e5813.jpg)

16.【解答】
- DHCP配置分析
  - 地址分配范围: 111.123.15.5~111.123.15.254
  - DHCPDiscover报文
    - 源IP: 0.0.0.0
    - 目的IP: 255.255.255.255

- MAC地址使用
  - 第一个以太网帧目的MAC: ff-ff-ff-ff-ff-ff
  - Internet访问帧目的MAC: 00-a1-a1-a1-a1-a1

- 主机1访问限制分析
  - 可访问WWW服务器
  - 不能访问Internet
  - 原因:默认网关配置错误(111.123.15.2)

17.【解答】
- 网络地址规划
  - 广播地址计算
    - 销售部广播地址: 192.168.1.127
    - 技术部子网地址: 192.168.1.128
  - 可分配主机数计算
    - 总可分配数: 126
    - 已分配数: 81
    - 剩余可分配: 45

- IP分片分析
  - MTU=800B
  - 分片大小计算
    - 最大分片数据: 776B
    - 分片数: 2
    - 第一分片偏移: 0
    - 第二分片偏移: 97

18.【解答】
- NAT配置
  - R2 NAT表设置
    ![](https://cdn-mineru.openxlab.org.cn/model-mineru/prod/06ca30ef7a3d3ce631cd6cb3500366e19978fe7921c9ce9bf04a5bfb1e77b7a8.jpg)

- IP地址转换过程
  - H2发送P
    - 源IP: 192.168.1.2
    - 目的IP: 203.10.2.2
  - R3转发后
    - 源IP: 203.10.2.6
    - 目的IP: 203.10.2.2
  - R2转发后
    - 源IP: 203.10.2.6
    - 目的IP: 192.168.1.2

19.【解答】
- 网络设备选择
  - 设备1: 100BaseT以太网交换机
  - 设备2: 100BaseT集线器

- 最短帧长分析
  - 发送时间计算: 5.12μs
  - 时延分析
    - 单程总时延: 2.56μs
    - Hub转发时延: 1.51μs
    - 传播时延: 1.05μs
  - 最大距离: 210m

- DHCP报文分析
  - M为DHCP发现报文
  - 广播特性
    - 目的MAC地址: FF-FF-FF-FF-FF-FF

- 帧地址分析
  - 地址1(接收方H5): 00-11-11-11-11-E1
  - 地址2(AP): 00-11-11-11-11-C1
  - 地址3(发送方H4): 00-11-11-11-11-D1

# 4.3.6 答案与解析  

# 单项选择题  

# IPv6相关特性
- 地址长度与空间
  01.D
  - IPv6地址用16B（128比特）表示
  - 地址空间是IPv4的 $2^{96}$ 倍

- IPv6首部特点
  02.D
  - 采用128位地址
  - 首部仅包含8个字段
  - 支持QoS，满足实时多媒体通信需求
  - 取消检验和字段
    - 网络传输介质可靠性高
    - 数据链路层和传输层有检验机制

- IPv6地址表示规则
  03.C
  - 零压缩法规则
    - 双冒号":"只能在地址中出现一次
    - 多处不相邻的0只能用":"代表一处

  04.D
  - 冒号十六进制记法规则
    - 多个连续0区域可零压缩，但仅可出现一次
    - 每区域开头的0可省略，结尾0不可省略
    - 每区域应有4位十六进制数

- IPv6首部简化
  05.D
  - 首部长度固定，无需首部长度字段
  - 取消检验和字段加快处理速度
  - 依赖链路层和传输层的差错处理机制

- IPv6分片处理
  06.A
  - 不允许分片
  - 数据报过大时
    - 路由器丢弃该数据报
    - 向发送方发送ICMP报文指示分组太大

- IPv4与IPv6对比
  07.D
  - 地址空间
    - IPv4: 32位，$2^{32}$
    - IPv6: 128位，$2^{128}$
  - 首部长度
    - IPv4: 可变，4B倍数
    - IPv6: 固定40B
  - 过渡技术
    - 双协议栈
    - 隧道技术
  - 共同点
    - HopLimit字段(IPv6)和TTL字段(IPv4)功能相同



# 4.4.7 答案与解析  

# 一、单项选择题  

# 路由选择基础
- 静态路由选择与动态路由选择
  01.B
  - 静态路由选择特点
    - 使用手动配置路由信息
    - 实现简单且开销小
    - 需要维护整个网络拓扑结构信息
    - 不能及时适应网络状态变化
  - 动态路由选择特点
    - 通过路由选择协议自动发现维护路由信息
    - 能及时适应网络状态变化
    - 实现复杂且开销大
  - 两者都使用路由表

  02.B
  - 静态路由(非自适应算法)
    - 不会根据流量和结构调整路由决策
    - 用户可随时配置路由表
  - 动态路由(自适应算法) 
    - 需要实时获取网络状态
    - 根据网络状态适时改变路由决策

# 路由选择算法
- 链路状态算法
  03.A
  - 工作原理
    - 路由器在链路状态变化时用洪泛法发送信息
    - 发送信息包括相邻路由器和链路状态
  - 优点
    - 快速收敛
    - 及时重新计算路由
    - 保持链路状态表一致性

  04.B
  - 实现过程
    - 交换结点到邻居结点的代价构建网络拓扑
    - 使用Dijkstra算法计算最短路径

- 分层路由
  05.B
  - 特点
    - 路由器被划分为区域
    - 只知道本区域内的路由信息
    - 不同网络可作为独立区域
    - 无需知道其他网络拓扑结构

  06.B
  - 优点
    - 限制洪泛法范围在区域内
    - 减少通信量
    - 适用于大规模自治系统
  - 缺点
    - 交换信息种类增多
    - OSPF协议更复杂

# 路由选择协议
- 基本功能
  07.D
  - 获取网络拓扑信息
  - 构建路由表
  - 更新路由信息
  - 选择最优路径
  - 识别无环通路
  - 不包括发现下一跳物理地址

  08.B
  - BGP是域间路由协议
  - RIP和OSPF是域内路由协议
  - ARP不是路由协议

- RIP协议
  09.A
  - 最大跳数为15
  - 16表示网络不可达

  10.D
  - 每经过一个路由器距离加1

  11.C
  - 只向相邻路由器发布路由信息
  - 不向整个域洪泛

  12.A
  - 路由更新机制
    - 收到更优路由时更新路由表
    - 向其他相邻路由器广播新路由

  13.
  - 收敛概念
    - 路由器调整路由表适应网络变化
    - 最终达到稳定状态
    - 收敛越快适应变化越快

  14.A
  - 属于应用层协议
  - 使用UDP传送数据

- OSPF协议
  15.A
  - 使用Hello分组保持邻居连接

  16.A
  - 用于自治系统内
  - 基于链路状态算法
  - 适用大型全局IP网络
  - 支持可变长子网掩码
  - 只在网络变化时传送更新报文

  17.B
  - 区域划分优点
    - 减少链路状态数据包数量和大小
    - 提高网络效率和稳定性
    - 路由器只需知道本区域拓扑

  18.D
  - 主干区域路由器
    - 区域边界路由器连接主干和下层区域
    - 主干路由器可兼作区域边界路由器

- BGP协议
  19.A
  - 特点
    - 寻找较好路由而非最佳路由
    - 交换到达目的网络的自治系统序列

  20.D
  - 各协议比较
    - RIP: 基于距离向量,使用跳数度量
    - OSPF: 使用链路状态协议,Dijkstra算法
    - BGP: 采用路径向量协议,寻找较好路由

21.B  

RIP和BGP协议属于应用层，OSPF和ICMP协议属于网络层。  

22.B  

距离-向量路由算法要求每个路由器维护一张路由表，该表给出了到达每个自的地址的已知最佳距离（最小代价）和下一步的转发地址。算法要求每个路由器定期与所有相邻路由器交换整个路由表，并更新自己的路由表项。注意从邻接结点接收到路由表不能直接进行比较，而要加上相邻结点传输消耗后再进行计算。C到B的距离是6，于是从C开始通过B到达各结点的最短距离向量是(11,6,14,18,12,8)。同理，通过D和E的最短距离向量分别是(19,15,9,3,12,13)和(12，11,8,14,5，9)。于是，C到所有结点的最短路径应该是 $(11,6,0,3,5,8)$  

23.C  

根据OSPF算法，从A到B转发经过的链路代价依次为2、3、1、1、2，一共经过4个路由器。分组长度为1000B，首部长度为20B，数据长度为980B，所以共有 $980000/980\,=\,1000$ 个分组，每次存储转发时延为 $1000\mathrm{B}{\div}100\mathrm{M}\mathrm{b}/\mathrm{s}=0.08\mathrm{ms}$ ，第一个分组从A到B的时间为 $0.08{\times}5=0.4\mathrm{ms}$ 剩下的999个分组每经过 $0.08\mathrm{ms}$ 就到达一个，所以总时间为 $0.4+0.08{\times}999=80.32\mathrm{ms}$  

24.D  

R1在收到信息并更新路由表后，若需要经过R2到达netl，则其跳数为17，因为距离为16表示不可达，所以R1不能经过R2到达netl，R2也不可能到达net1。选项B、C错误，选项D正确。而题目中并未给出R1向R2发送的信息，因此选项A也不正确。  

25.B  

初始收敛时，R3到网络（201.1.2.0/25）的距离为1，R2到网络的距离为2，R1到网络的距离为2。当R3检测到网络不可达时，因为R3存有其他邻居到网络的路由信息，所以它利用所有邻居的距离向量，用Bellman-Ford公式更新自己的距离向量（易错警告：误以为R3检测到网络不可达时，就把其到网络的距离设置为16），R3重新计算到网络的距离 $=\operatorname*{min}\{16,\mathrm{R}1$ 到网络的距离 $+\,1,\mathrm{R}2$ 到网络的距离 $+\left.1\right\}=\left\{16,2+1,2+1\right\}=3.$ 然后，R3向其所有邻居发送更新报文，“告诉它到网络的距离为3”。R2（及R1）收到R3发来的更新报文后，会利用它保存的所有邻居的距离向量，重新计算自己到网络的距离 $=\operatorname*{min}\{{\mathrm{R1}}$ 到网络的距离 $+\,1,\mathrm{R}3$ 到网络的距离 $+\left.1\right\}=\left\{2+\begin{array}{l l}\end{array}\right.$  $1,3+1\}=3$ ，因此答案为3。与此同时，R1也重新计算自己到网络的距离 $=\operatorname*{min}\{{\mathrm{R}}2$ 到网络的距离 $+\,1,\mathrm{R}3$ 到网络的距离 $+\left.1\right\}=\left\{2+1,\,3+1\right\}=3.$ 如此反复，直至重新收敛。因为RIP的特点“坏消息传得慢”，所以一旦网络出现故障，就要经过较长时间才能将故障消息传送到所有路由器。  

26.D  

RIP是一种分布式的基于距离向量的路由选择协议，它通过广播UDP报文来交换路由信息。OSPF是一个内部网关协议，要交换的信息量较大，应使报文的长度尽量短，所以不使用传输层协议（如UDP或TCP），而直接采用IP。BGP是一个外部网关协议，在不同的自治系统之间交换路由信息，因为网络环境复杂，需要保证可靠传输，所以采用TCP。因此，答案为选项D。  

27.D  

根据距离向量路由算法，E收到相邻路由器的距离向量后，更新它的路由表： $\textcircled{\scriptsize{1}}$ 当原路由表中没有目的网络时，把该项目添加到路由表中。  
$\circledcirc$ 发来的路由信息中有一条到达某个目的网络的路由，该路由与当前使用的路由相比，有较短的距离，就用经过发送路由信息的结点的新路由替换。  

分析题意可知，E与邻居路由器A、B、C和D之间的直接链路距离分别是8,10，12和6。到达Netl～Net4没有直接链路，需要通过邻居路由器。从上述算法可知，E到达目的网络一定是经过A、B、C和D中距离最小的。根据题中所给的距离信息，计算E经邻居路由器到达目的网络 $\mathrm{{Nuel}\!\sim\!\mathrm{{Nuet}}4}$ 的距离，如下表所示，选择到达每个目的网络距离的最短值。  

![](https://cdn-mineru.openxlab.org.cn/model-mineru/prod/2c98edc6ec159d059a6047008e7bec9026a74a414f84d9bb44109c347ec0158e.jpg)  

所以距离分别是9,20,28，20。  

# 二、综合应用题  

01.【解答】
- RIP、OSPF和BGP的协议层次对比
  - RIP位于UDP上层
    - 路由信息封装在UDP数据报中
  - OSPF位于网络层
    - 信息量大需短报文
    - 直接采用IP
  - BGP使用TCP
    - 跨自治系统通信
    - 复杂网络环境需可靠传输

- 内部网关协议与BGP的区别
  - 内部网关协议特点
    - 关注自治系统内部效率
    - 无需考虑其他策略
  - BGP特点
    - 互联网规模大导致路由选择困难
    - 不追求最佳路由
    - 需考虑自治系统间策略
    - 无需周期性交换路由信息

02.【解答】
- RIP路由表更新规则
  - 从C收到路由信息处理
    - 下一跳改为C
    - 每个距离加1
  - 更新规则
    - 目的网络相同且下一跳相同时直接更新
    - 新目的网络则增加表项
    - 目的网络相同但下一跳不同且距离更短则更新
    - 其他情况无操作

![](https://cdn-mineru.openxlab.org.cn/model-mineru/prod/191f4d1c97abfc4666640bda25ef942d88ffc01cce7dd7df1e4b72cb934b0a9a.jpg)

![](https://cdn-mineru.openxlab.org.cn/model-mineru/prod/10a663113dd459280ab4ae2ced987abfb63e217753cf47d488c4ba39e9728f86.jpg)

- 网络不可达情况处理
  - B到N2距离为16表示不可达
  - 应丢弃IP分组并报告源主机

03.【解答】
- 路由器端口代价说明
  - 代表转发分组的代价
  - 同一链路两端代价可能不同
  - 直连路由器间无需中间路由

- R6到N1路径代价计算
  - R6到R3代价为6
  - R3到R1代价为1 
  - R1到N1代价为3
  - 总代价为10

- Dijkstra算法应用
  - 结点加入次序示例
  - R6路由表如下

![](https://cdn-mineru.openxlab.org.cn/model-mineru/prod/8e92ef2e53e7e853e5911ed198c1c39d755663a23aebbec097dcad8f0999f813.jpg)

04.【解答】
- 路由聚合要求
  - AS1中聚合
    - 153.14.5.0/25和153.14.5.128/25聚合为153.14.5.0/24
  - AS2中聚合
    - 194.17.20.0/25和194.17.21.0/24聚合为194.17.20.0/23
    - 194.17.20.128/25保持独立

- R2路由表

![](https://cdn-mineru.openxlab.org.cn/model-mineru/prod/4dfb2175582c3dce552f3313306db765865d85fe89b9aa9d1bb38f7f5029358b.jpg)

- IP分组转发
  - 目的地址194.17.20.200匹配两个表项
  - 根据最长匹配原则通过E0接口转发

- R1和R2间路由协议
  - 使用BGP/BGP4交换路由信息
  - BGP报文封装在TCP段中

05.【解答】
- 路由聚合处理
  - 同接口转发网络聚合
    - 192.1.6.0/24和192.1.7.0/24通过L0接口
    - 聚合为192.1.6.0/23
  - 路由表如下

![](https://cdn-mineru.openxlab.org.cn/model-mineru/prod/cf4ddf048e138ddec474ac62014277fa6bae3b900576bbe39c81b814cb3542f1.jpg)

- IP分组TTL计算
  - R1通过L0接口转发
  - 经过3个路由器
  - 最终TTL为61(64-3)

- 默认路由配置
  - 互联网路由采用默认路由
  - 网络前缀为0.0.0.0/0
  - LSI需增加特殊直连网络
    - Prefix为"0.0.0.0/0"
    - Metric为10

# 4.5.6 答案与解析  

# 一、单项选择题  

01.D
- 多播与单播比较
  - 多播带宽优势
    - 多播所需带宽小于多个单播带宽之和
  - 时延对比
    - 多个单播仿真时路由器时延大
    - 处理单个多播分组时延小

02.B
- 多播转发树特性
  - 避免环路
    - 树结构无环路特性
    - 可将多播分组传送到组内每台主机
  - 其他机制
    - 水平分割用于避免距离-向量路由算法中的无穷计数问题
    - TTL字段防止IP分组环路无限循环

03.A
- 以太网多播地址映射
  - 地址块范围
    - 01-00-5E-00-00-00~01-00-5E-7F-FF-FF
  - 映射规则
    - 每个地址只有后23位可用于多播
    - 与D类IP地址后23位一一对应
    - D类IP地址可分配28位,前5位不用于构成以太网硬件地址
  - 映射示例
    - 215的二进制11010111,最高位映射为0
    - 215.145.230映射为01010111.10010001.11100110
    - 对应十六进制57-91-E6

04.B
- 多播地址范围
  - 点分十进制表示范围
    - 224.0.0.0~239.255.255.255
  - 选项B在有效区间内
# 二、综合应用题  

01.【解答】

- 互联网多播实现
  - 路由器实现方式
    - 需增加识别多播软件
    - 可以是专用多播路由器
    - 可以是运行多播软件的普通路由器

- 互联网多播与以太网多播对比
  - 互联网多播更复杂
    - 以太网本身支持广播和多播
    - 当前互联网路由器大多不支持广播和多播
    - 许多物理网络不支持广播和多播

# 4.7.5 答案与解析  

# 一、单项选择题  

01.B
- 网桥和交换机特点
  - 第二层设备
  - 能够分割冲突域
  - 不能分割广播域
- 路由器特点  
  - 第三层设备
  - 不转发全网广播(目的地255.255.255.255)
  - 可以分割广播域

02.C
- 冲突域定义
  - 能产生冲突的所有设备的集合
  - 设备同时发送数据会发生信号干扰和冲突
- 冲突域大小决定因素
  - 网络拓扑
  - 设备类型

03.C
- 局域网互连需求
  - 需要路由器作为连接设备
  - 远程局域网需要广域网技术

04.C
- 路由器功能层次
  - 必须处理网络层以下功能
    - 物理层
    - 数据链路层
  - 不实现网络层以上功能
    - 传输层
    - 应用层

05.C
- 路由器特性
  - 转发速度比交换机慢
  - 路由选择参数多样
  - 只能根据IP地址转发

06.B
- 路由选择方式
  - 直接交付
    - 发送站与目的站在同一网段
  - 间接交付
    - 最后一个路由器需直接交付
    - 不在同一网段时使用
    - 不涉及路由器

07.D
- 交付方式判断
  - 根据分组目的IP地址和路由器接收端口IP地址判断
  - 判断过程
    - 源IP地址和目的IP地址分别与子网掩码"与"操作
    - 得到相同子网地址则直接交付
    - 不同则间接交付

08.C
- 路由表特点
  - 包含到目的网络的下一跳路径信息
  - 不包含所有主机的下一跳信息

09.C
- 转发表生成
  - 根据路由表生成
  - 路由表由路由算法决定
  - 路由算法决定转发表值

10.D
- 路由选择处理机任务
  - 根据路由选择协议构造路由表
  - 与相邻路由器交换路由信息
  - 更新维护路由表

11.D
- 分组转发部分组成
  - $\textcircled{\scriptsize{1}}$ 交换结构
    - 根据转发表处理分组
    - 从输入端口转发到输出端口
  - $\circledcirc$ 输入端口
    - 包括物理层、数据链路层和网络层处理模块
  - $\textcircled{3}$ 输出端口
    - 接收分组
    - 发送到外部线路

12.D
- 路由器端口功能
  - 包含三层处理模块
    - 物理层
    - 数据链路层
    - 网络层
  - 输入端口处理
    - 物理层接收比特流
    - 数据链路层提取帧
    - 网络层处理分组
  - 输出端口处理
    - 执行相反操作
    - 根据目的地址查找转发表
    - 决定输出端口

13.D
- 路由选择部分组成
  - $\textcircled{\scriptsize{1}}$ 路由选择处理机
    - 构造路由表
    - 交换路由信息
  - $\circledcirc$ 路由选择协议
    - 更新路由表算法
  - $\textcircled{3}$ 路由表
    - 根据路由算法得出
    - 包含目的网络到下一跳映射

14.C
- 路由器延迟特点
  - 实现三层功能
    - 物理层
    - 数据链路层
    - 网络层
  - 传输延迟时间最长

15.C
- 默认路由特点
  - 目的地址为0.0.0.0
  - 子网掩码为0.0.0.0

16.D
- 输出端口特点
  - 是路由器接口
  - 每个接口有标识符
  - 路由表指定接口标识符
  - 根据标识符确定输出端口

17.A
- 广播域特点
  - 交换机转发广播帧
    - 同一交换机下设备在一个广播域
  - 路由器不转发广播帧
    - 工作在网络层
    - 只关心IP地址
    - 不关心MAC地址

18.C
- 设备传输时延比较
  - 路由器
    - 时延最大(几千微秒)
    - 需处理IP地址
    - 软件完成处理
  - 交换机和网桥
    - 时延较小
    - 交换机几十微秒
    - 网桥几百微秒
    - 硬件转发
  - 集线器
    - 时延最小
    - 立即转发信号

19.D
- 网络设备特点
  - 中继器和集线器(物理层)
    - 不隔离冲突域
    - 不隔离广播域
  - 网桥和交换机
    - 分隔冲突域
    - 不隔离广播域
    - 冲突域等于端口个数
    - 广播域为1
  - 路由器
    - 隔离广播域和冲突域
    - 屏蔽数据链路层广播帧

20.C
- 路由器功能
  - 监测拥塞处理
    - 合理丢弃IP分组
    - 发送源点抑制ICMP报文
  - IP分组处理
    - 首部差错检验
    - 丢弃错误首部报文
    - 不保证分组不丢失

21.C
- 网络设备隔离域能力
  - 路由器(网络层)
    - 隔离广播域和冲突域
  - 交换机(数据链路层)
    - 只隔离冲突域
  - 集线器、中继器(物理层)
    - 不隔离广播域
    - 不隔离冲突域
- 总计
  - 2个广播域
  - 4个冲突域

![](https://cdn-mineru.openxlab.org.cn/model-mineru/prod/3bd3a53a42f3e93b1f2c9245202cb90dceb0e91ce15adcbc69866f3b96ff6394.jpg)

# 二、综合应用题  

01.【解答】

- 路由表分析
  - 将H1、H2、H3、H4的IP地址与子网掩码进行"与"操作
  - 得到4个子网的网络地址
    - 202.99.98.16
    - 202.99.98.32  
    - 202.99.98.48
    - 202.99.98.64
  - 路由器R1到4个子网的路由表如下

![](https://cdn-mineru.openxlab.org.cn/model-mineru/prod/7b1f4342bf382bf42fc2fa6680386796983134a7977d5ee5138fef074ce8e3e3.jpg)

- H1向H2发送IP数据报过程
  - 步骤1: H1构造IP数据报
    - 源IP: 202.99.98.18
    - 目的IP: 202.99.98.35
    - 判断不在同一子网,无法直接交付
  - 步骤2: H1获取MAC地址
    - 通过ARP获取路由器R1(202.99.98.17)的MAC地址
    - 封装帧头:目的MAC为R1,源MAC为H1
  - 步骤3: R1处理数据报
    - 去除帧头帧尾获取IP数据报
    - 查找路由表,确定下一跳为直接相连
  - 步骤4: R1转发数据报
    - 通过ARP获取H2的MAC地址
    - 封装新帧:目的MAC为H2,源MAC为R1
  - 步骤5: H2接收数据报
    - 去除帧头帧尾
    - 获取H1发来的IP数据报

> attention:
在步骤2中,帧的目的MAC地址为默认网关MAC地址;在步骤4中,帧的源MAC地址为默认网关MAC地址

02.【解答】

- 转发概念
  - 处理到达的分组
  - 查找路由表确定输出线路
  - 将分组发送到正确线路

- 路由算法特点
  - 是网络层软件组成部分
  - 确定分组传送的输出线路
  - 负责填充和更新路由表
  - 转发功能根据路由表确定分组处理方式

03.【解答】

- 网络设备分析
  - 设备类型判断
    - 设备1为路由器:可连接不同LAN/WAN,隔离广播域
    - 设备2、3为以太网交换机:同一广播域
  - IP地址划分
    - LAN1: 192.168.1.2/26和192.168.1.3/26
    - LAN2: 192.168.1.66/26和192.168.1.67/26

- 接口配置
  - IF1接口
    - 与路由器R相连
    - IP地址:192.168.1.254
  - IF2、IF3接口
    - IF2: 192.168.1.1(LAN1默认网关)
    - IF3: 192.168.1.65(LAN2默认网关)

- 私有地址分析
  - C类地址段:192.168.0.0~192.168.255.255
  - H1~H4均为私有IP地址
  - 访问Internet需R提供NAT服务

- 广播域隔离
  - H3发送目的地址192.168.1.127的数据报
  - 为本网络广播地址
  - 路由器隔离广播域
  - 只有H4能接收到数据报