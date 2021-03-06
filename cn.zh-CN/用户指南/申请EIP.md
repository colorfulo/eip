# 申请EIP {#task_bh5_dll_vdb .task}

创建EIP后，您可以将EIP作为一个公网IP绑定到需要的资源上。

1.   登录[专有网络管理控制台](https://vpcnext.console.aliyun.com)。 
2.   登录[专有网络管理控制台](https://partners-intl.console.aliyun.com/#/vpc)。 
3.   单击**申请弹性公网IP**，根据以下信息选择您的配置，然后单击立即支付并完成支付。 

    |配置|说明|
    |:-|:-|
    |**计费方式**| EIP支持预付费和后付费（按量付费）两种计费方式：

     -   **预付费**：采用包年包月的售卖方式，按固定带宽计费。

在合同期内，EIP实例只支持升级配置，不支持降级配置或者释放。详细信息参见[预付费](../cn.zh-CN/产品定价/预付费.md#)。

    -   **按量付费**：支持按使用流量和按固定带宽两种计费方式。

后付费EIP实例可以随时进行变配和释放。详细信息[按量付费](../cn.zh-CN/产品定价/按量付费.md#)。

 |
    |**地域**| 选择EIP的地域。

 请确保EIP的地域和待绑定的资源（ECS实例、NAT网关或SLB实例）的地域相同。

 |
    |**带宽峰值**|根据您的业务需要，设置EIP的带宽峰值。|
    |**计费方式**| 选择按流量计费还是按固定带宽计费。该选项只适用于后付费实例。

     -   **按使用流量计费**：根据每小时访问公网的实际流量计费。

    -   **按固定带宽计费**：由带宽值决定每日账单价格，与实际使用的流量无关。

 |
    |**购买数量**|根据业务需要，选择购买EIP的数量。|


