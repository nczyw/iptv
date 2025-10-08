# 江苏电信IPTV最新组播地址
* 更新日期:2025年10月8日
  - 只保留高清及以上的源
* 不定期更新
## openwrt抓包方法,假设机顶盒插在`eth1`上,该方法只针对江苏电信
 - 机顶盒保持关闭
 - 路由器上运行:`tcpdump -i eth1 -n -s 0 -w /tmp/eth1_all.pcap`
 - 打开机顶盒,等待开机进入主界面,完成后关闭机顶盒即可
 - 路由器`Ctrl+C`停止抓包,把`/tmp/eth1_all.pcap`复制到地址电脑上使用`Wireshark`打开
 - 应用过滤中输入`http`,再按`Ctrl+F`查找,选择`分组详情`和`字符串`,查找内容填`jsSetConfig`,查找,第一个很可能就是节目表
 - `右键`-`追踪流`-`HTTP Stream`里面的`jsSetConfig`就是所有节目表