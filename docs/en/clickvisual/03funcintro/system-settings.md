# System Settings

After ClickVisual deployment, the first thing to do is to configure the Kubernetes cluster and ClickHouse data source.

## 1. Instances Management

In the top nav bar,select **Setting -> Cluster：**

![img.png](../../images/instance-list.png)

As we haven't configure any clusters yet, the list is empty.Click **+Add cluster**,Fill in the pop-up form with the cluster information to be configured, including cluster name, API server address, Kube-config, etc. 

![img.png](../../images/k8s-create.png)

After submission, it can be used for the distribution of LogAgent configuration.

## 2. ClickHouse data source management

In the top nav bar,select **Setting -> Instances：**

![img.png](../../images/instance-list.png)

By default, no data source instance is configured, so this is blank,click **+Add instance**, add a new ClickHouse instance as datasource.

datasource config like that
> `tcp://x.x.x.x:9000?username=x&password=x&read_timeout=10&write_timeout=20&debug=true`


|parameter| type    |
|---|-------|
|read_timeout| float |
|write_timeout| float |
|block_size| int   |
|compress| bool  |

![img.png](../../images/instance-create.png)

After configuring the `dev-clickhouse` data source, it can be used in the log query page later.