# ECS固定公网IP转换为EIP {#concept_jgg_1rm_vdb .concept}

您可以将专有网络ECS实例的固定公网IP转换为EIP，灵活管理公网IP的使用。

## 公网IP介绍 {#section_vrf_5rm_vdb .section}

阿里云的ECS如果需要通过互联网（公网）对外提供服务，让用户可以访问部署在ECS上的应用，就必须需要为ECS配置公网IP和公网带宽。

阿里云有两种类型的公网IP：

-   ECS固定公网IP

    当您在创建专有网络（VPC）类型的ECS实例时，如果选择使用系统分配的公网IP，创建后系统会为其分配一个公网IP，该公网IP无法与ECS解绑，称之为ECS的固定公网IP。

-   弹性公网IP

    弹性公网IP（EIP），是可以独立购买和持有的公网IP地址资源。目前，EIP可绑定到专有网络类型的ECS实例、专有网络类型的私网SLB实例和NAT网关上，还可以使用共享带宽和共享流量包等网络产品，节约公网使用成本。


无论是固定公网IP还是EIP，对外提供公网服务的能力是一样的，都是阿里巴巴优质的多线BGP网络。两者的最大区别就是是否可以和ECS实例解绑。EIP可以随时从ECS实例上解绑，在需要时重新绑定；固定公网IP无法从ECS实例上解绑。

## 转换为EIP的优势 {#section_abd_gsm_vdb .section}

固定公网IP会逐步被可解绑的EIP所替换。使用EIP有以下好处：

-   灵活应对DDoS攻击

    当您的服务器遭受到DDoS攻击时，您可以立刻将绑定到受攻击的ECS实例的EIP解绑，及时绑定新的EIP，配合使用云盾的高防IP，可以轻松化解DDoS攻击。

-   简化系统和应用的扩展

    当您的应用系统需要扩张，提升对外服务能力时，可能会将应用部署在多台ECS实例上然后使用SLB进行流量转发。因为EIP支持绑定VPC类型的SLB实例，此时您可以将EIP解绑，然后绑定到购买的VPC类型的SLB实例对外提供服务。整个系统架构升级对用户无感知。

-   节省成本

    配合使用共享带宽产品，可以大大减少EIP的公网成本。

    详情参见[如何节约公网成本](https://help.aliyun.com/document_detail/67459.html)。

-   简化网络权限管理

    您可以提交工单申请连续的公网IP地址，连续的公网IP地址可以简化网络权限管理。


## 转换限制 {#section_abt_psm_vdb .section}

要转换的ECS实例必须满足以下要求：

-   仅支持分配了公网IP地址的专有网络类型的ECS实例。

-   仅支持处于已停止（Stopped）或运行中（Running）的状态的ECS实例。

-   如果ECS实例有未生效的变更配置任务，不能进行转换。

-   对于包年包月的ECS实例，在实例到期前24小时内，不能进行转换。

-   按固定带宽计费的包年包月ECS实例，不能进行转换。


## 操作步骤 {#section_ghs_tsm_vdb .section}

完成以下操作，将专有网络类型的ECS实例的固定公网IP转为EIP：

1.  登录 ECS管理控制台。
2.  在左侧导航栏，单击 **实例**。
3.  选择地域，找到目标ECS实例。
4.  单击**更多** \> **公网IP转换为弹性公网IP** 。
5.  在弹出的对话框中，单击 **确定**。
6.  刷新实例列表。

    转换成功后，原来的公网IP地址会标注为**弹性**。

    ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/12809/2253_zh-CN.png)


