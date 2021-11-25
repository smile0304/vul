## Tenda AC15 app_data_center CMD Inject

Vulnerability for Tenda AC15 Router AC1900 Smart Dual-Band Gigabit WiFi Router

Product: Tenda AC15

Version: The lastest firmware -- V15.03.05.19_CN [Download](https://www.tenda.com.cn/download/detail-2680.html)

Vulnerability Type: Command Injection

### Vulnerability description

An issue was discovered on Tenda AC15 devices with firmware through V15.03.05.19_CN. A command Inject vulnerability allows attackers to execute arbitrary OS commands via shell metacharacters in a crafted POST request. This occurs when the `FUN_0000a6e8` function calls system to run operation with an untrusted input parameter named `dev_name`. Consequently, an attacker can execute any command remotely when they control this input. The details are as below:

![vul_detail](./img/1.png)

POC:

![poc](./img/2.png)