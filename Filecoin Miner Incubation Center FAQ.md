# Filecoin Miner Incubation Center FAQ
:pencil2: ***Welcome continuous supplement***

</br>

**1. 配置*venus*时如果出现`bad handshake`，访问失败怎么处理?**

需要修改 `~/.venus/config.toml` 中的listen IP为`0.0.0.0`默认是监听在本地`127.0.0.1`，然后重启*venus*。

</br>

**2. 新集群部署完成后*venus-sealer*没有下发任务如何处理？**

在*venus-auth*节点上使用`./venus-messager wallet list`命令查看集群的配置信息是否有误。

```sh
"Name": "venus",
"Url": "/ip4/xxx.xxx.xxx.xxx/tcp/5678/http",  # venus-wallet的地址和端口
"Token": "eyJhbGciOiJIUzIadraInR5cCI6IkpXVCJ,  # venus-wallet的api-info的token,可以使用`./venus-wallet-pro auth api-info --perm sign`命令获取wallet的token值
"State": "Alive",  # 连接状态
```
</br>

**3. *venus*节点宕机，或需要重启并导入badger文件时，如何切换到备用机？**

- *venus-messager:*

修改用户的默认目录下的`messager.toml`配置文件里的内容，指向新节点后，重启*venus-messager*服务。

```sh
# cat ~/messager.toml
[node]
url = "/ip4/192.168.1.134/tcp/3453"
token= "eyJhbGciOIUacbciIsInR5cCI6I.iLCJwZXJtIjoic2lnbiIs.c65GtR7IVjJYE"
```

kill掉之前的*venus-messager*进程后，再重新启动即可。

- *venus-miner:*

修改用户的默认目录下的配置文件连接的ip地址。

```sh
# cat ~/.venus-miner/config.toml
ListenAPI = "/ip4/192.168.0.98/tcp/3453/http"
oken = "eyJhbGciOiJIUzIsInR5c.eyJuYW1lIjoibWMmV4dCI6IiJ9.3P0x6StVjJYEhv198"
```
    
重新启动*venus-miner*服务。

*winning-post*和*venus-sealer*节点修改`.lotus/api`和`.lotus/token`的值。

```sh
$ cat .venus/api
/ip4/120.78.159.125/tcp/3453/http
 ```
修改完成后重启*winning-post*和*venus-sealer*。

</br>

**4. 地址余额不足且未及时处理，或*venus*节点出口流量饱和，导致大量任务卡在WaitSeed如何处理？**

在*venus-auth*节点上使用`./venus-messager msg list-fail`命令打开fail的消息，然后使用`./venus-messager msg mark-bad --really-do-it <失败消息id>`命令将fail的消息推回sealer侧重启并判断消息是否异常，然后再次检查是否还有fail的消息。

</br>

**5. *venus-miner*无法出块如何处理？**

确认*venus-miner*连接的*venus*节点高度同步是否正常，并检查其日志是否正常。

在*venus-miner*节点上使用`logs/venus-miner.log`查看日志信息。

使用`./venus-miner address state`命令确认IsMining为true

```sh
    # ./venus-miner address state
    [
    	{
    		"Addr": "f0xxx",     # 矿工号
    		"IsMining": true,    # 是否在挖矿（出块）
    		"Err": null          # 是否有报错信息
    	}
    ]
```

查看*venus-miner*的配置是否有误，主要查看*venus-sealer*和*venus-wallet*的ListenAPI及Token配置是否有问题。

```sh
    # ./venus-miner address list
    [
    	{
    		"Addr": "f0xxxx",
    		"Sealer": {
    			"ListenAPI": "/ip4/192.168.0.77/tcp/2345/http",
    			"Token": "eyJhbGciOiJIUzI1CJ9.eyJBbGxvdyIJpX0.HQZF5ksttTCrjgTVVOKv0"
    		},
    		"Wallet": {
    			"ListenAPI": "/ip4/192.168.0.94/tcp/5678/http",
    			"Token": "eyJhbJIUzI1NiIs9.eyJBbGxvdyI619.32efj05GQYhBllQ4gt05AC3AY"
    		}
    	}
    ]
```

</br>
    
**6. 连接本地数据库报错如何处理？**

Ubuntu v18.04中需要通过drop user `root'@'localhost`命令删除授权信息，再进行正常授权。

</br>

**7、*venus-wallet*日志出现‘WalletSign error password not set’错误如何处理？**

通过`./venus-wallet setpwd`设置密码（如果之前设置过，重启*venus-wallet*后需要重新输入之前设置的密码，即重新设置密码）

</br>

## *Note* 

:pencil2: ***Welcome continuous supplement***

</br>

1. 关于*venus*组件，需要**定期检查venus组件的同步情况**。

2. 关于*venus-sealer*组件，**当sectors出现过期的情况时，需要手动把过期的任务重制**。

3. *venus-sealer*下发的任务过多可能会导致一些异常的问题。

4. *venus-sealer*暂时还没有支持windows-post时间显示，**您可能需要其他的方式获取时间**。

5. 关于*venus-wallet*，密码是存在内存中的，所以**每次重启您都需要运行`set-password`命令来设置密码**。

6. 您可能会遇到**消息上链错误的日志，这些消息可能会堵塞您的消息池，*venus*的维护人员需要定期做处理**，如果没有及时处理，您需要联系venus的维护人员。
