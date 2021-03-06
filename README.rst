Python Apollo Clinet
====================

.. contents:: 目录:
   :local:

安装
----
::

    cd /usr/share/pyshared
    git clone http://172.18.200.207/apollo/python-apolloclient.git
    cd /usr/lib/python2.7/dist-package
    ln -s /usr/share/pyshared/python-apolloclient/apolloclient


物理机信息API(Node information API)
-----------------------------------

数据结构： 
::

   id                        ---id号
   hostname                  ---主机名
   cpu_count                 ---CPU核数
   cpu_info                  ---CPU信息
   ip                        ---主机IP地址
   disk_size                 ---磁盘容量
   memory_size               ---内存容量
   ipmi                      ---IPMI信息
   ipmi_check                ---IPMI状态
   power_stats               ---电源状态
   updated_at                ---记录更新时间
   

1.获取物理机信息

``调    用： client.nodes.get(node_id)``
``参    数： node_id                   ---nodes表中的id号``
``返 回 值： <warlock.core.node object>``

   
例：
::

    >>> import apolloclient.v1 import client
    >>> c = clinet.Client("http://10.33.24.2:34555")
    >>> node = c.nodes.get(1)

结果：
::

    >>> print node
    <warlock.core.node object at 0x1d4aa90>
