# Ansible Tower的介绍

Ansible Tower是一个中心化的管理节点网站，需要解决企业级的 用户的两个难题，一个是直接在每个管理员自己的电脑上放置ssh有安全的隐患，另外一个是如果有新管理员加入，面对海量的机群配置ssh连接有工作量巨大，效率低下。

作为一个ansilbe管理节点网站，那么它自然应该具备两个方面的功能：

1. 像其它管理网站一样，具有用户的创建和权限管理的功能；
2. 像ansible管理节点一样，配置远程主机的连接，放置playbook脚本
3. 此外，比ansible管理节点更强大的是tower还可以记录每个playbook的执行状态，从而从用户角度，或者以主机为对象统计执行状态。

另外如果需要解决企业级用户用户面对的安全和效率问题，tower就需要有两个角色，一个是管理员，另外一个是用户。tower管理员可以创建和管理ssh的连接的key文件，用户只能使用ssh连接，而对于一些ssh的key文件和密码则不可见。
