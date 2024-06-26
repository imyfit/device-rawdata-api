# 原始数据API

| 版本  |   日期   |                    备注                    |
| :---: | :------: | :----------------------------------------: |
| 1.0.0 | 20220318 | 对该版本之前的所有版本进行整理，形成此文档 |
| 1.0.1 | 20230620 |            增加NB/CAT1远程协议             |
| 1.0.2 | 20230728 |     NB/CAT1传输协议，传输中更改为0x03      |

1. 本协议文档可能不是最新版本；

2. 本协议文档描述，原始数据接口相关协议；

3. 开发者若需要硬件对接请联系销售人员,  https://www.imyfit.com ；

4. 若协议文档有更新，不再另行通知，强烈建议开发者到 https://imyfit.gitee.io 获取在线最新协议；

5. 若有疑问请到ISSUE区提出 https://gitee.com/imyfit/imyfit-issue 愿我们的付出对您的开发事半功倍。



## 传感器配置



### 2.1 PPG类型-0x01

Table 1 PPG控制参数表

<table>
  <tr>
  	<td>Name</td>
    <td colspan="4">Content</td>
  </tr>
  <tr>
  	<td>Bit</td>
    <td>7</td>
    <td>6</td>
    <td>5</td>
    <td>4</td>
  </tr>
  <tr>
  	<td>Default Value</td>
    <td>0</td>
    <td>0</td>
    <td>0</td>
    <td>0</td>
  </tr>
  <tr>
  	<td>Content</td>
    <td>ble_transmit</td>
    <td>nb_transmit</td>
    <td>reserved</td>
    <td>reserved</td>
  </tr>
  <tr>
  	<td>Bit</td>
    <td>3</td>
    <td>2</td>
    <td>1</td>
    <td>0</td>
  </tr>
  <tr>
  	<td>Default Value</td>
    <td>0</td>
    <td>0</td>
    <td>0</td>
    <td>0</td>
  </tr>
  <tr>
  	<td>Content</td>
    <td>ir_en</td>
    <td>red_en</td>
    <td>green_en</td>
    <td>onoff</td>
  </tr>
</table>

ble_transmit： ‘1’使能蓝牙数据传输

nb_transmit：‘1’使能NB/CAT1数据传输(暂不支持)

ir_en： ‘1’使能IR LED(仅onoff‘1’时有效)

red_en：‘1’使能Red LED(仅onoff‘1’时有效)

green_en：‘1’使能Green LED(仅onoff‘1’时有效)

onoff： ‘1’开启传感器(若传感器未开启则会立即打开)

### 2.2 ECG类型-0x02

Table 2 ECG控制参数表

<table>
  <tr>
  	<td>Name</td>
    <td colspan="4">Content</td>
  </tr>
  <tr>
  	<td>Bit</td>
    <td>7</td>
    <td>6</td>
    <td>5</td>
    <td>4</td>
  </tr>
  <tr>
  	<td>Default Value</td>
    <td>0</td>
    <td>0</td>
    <td>0</td>
    <td>0</td>
  </tr>
  <tr>
  	<td>Content</td>
    <td>ble_transmit</td>
    <td>nb_transmit</td>
    <td>reserved</td>
    <td>reserved</td>
  </tr>
  <tr>
  	<td>Bit</td>
    <td>3</td>
    <td>2</td>
    <td>1</td>
    <td>0</td>
  </tr>
  <tr>
  	<td>Default Value</td>
    <td>0</td>
    <td>0</td>
    <td>0</td>
    <td>0</td>
  </tr>
  <tr>
  	<td>Content</td>
    <td>reserved</td>
    <td>reserved</td>
    <td>reserved</td>
    <td>onoff</td>
  </tr>
</table>

ble_transmit： ‘1’使能蓝牙数据传输

nb_transmit：‘1’使能NB/CAT1数据传输(暂不支持)

onoff：‘1’开启传感器(若传感器未开启则会立即打开)

### 

### 2.3 IMU类型-0x03

Table 3 Gsensor控制参数表

<table>
  <tr>
  	<td>Name</td>
    <td colspan="4">Content</td>
  </tr>
  <tr>
  	<td>Bit</td>
    <td>7</td>
    <td>6</td>
    <td>5</td>
    <td>4</td>
  </tr>
  <tr>
  	<td>Default Value</td>
    <td>0</td>
    <td>0</td>
    <td>0</td>
    <td>0</td>
  </tr>
  <tr>
  	<td>Content</td>
    <td>ble_transmit</td>
    <td>nb_transmit</td>
    <td>reserved</td>
    <td>reserved</td>
  </tr>
  <tr>
  	<td>Bit</td>
    <td>3</td>
    <td>2</td>
    <td>1</td>
    <td>0</td>
  </tr>
  <tr>
  	<td>Default Value</td>
    <td>0</td>
    <td>0</td>
    <td>0</td>
    <td>0</td>
  </tr>
  <tr>
  	<td>Content</td>
    <td>Mag_en</td>
    <td>Gyr_en</td>
    <td>Acc_en</td>
    <td>onoff</td>
  </tr>
</table>

ble_transmit：‘1’使能蓝牙数据传输

nb_transmit： ‘1’使能NB/CAT1数据传输(暂不支持)

Mag_en：‘1’使能加速计(仅onoff‘1’时有效)

Gyr_en：‘1’使能陀螺仪(仅onoff‘1’时有效)

Acc_en： ‘1’使能磁力计(仅onoff‘1’时有效)

onoff ：‘1’开启传感器(若传感器未开启则会立即打开)

### 2.4 GNSS类型-0x05

<table>
  <tr>
  	<td>Name</td>
    <td colspan="4">Content</td>
  </tr>
  <tr>
  	<td>Bit</td>
    <td>7</td>
    <td>6</td>
    <td>5</td>
    <td>4</td>
  </tr>
  <tr>
  	<td>Default Value</td>
    <td>0</td>
    <td>0</td>
    <td>0</td>
    <td>0</td>
  </tr>
  <tr>
  	<td>Content</td>
    <td>ble_transmit</td>
    <td>nb_transmit</td>
    <td>reserved</td>
    <td>reserved</td>
  </tr>
  <tr>
  	<td>Bit</td>
    <td>3</td>
    <td>2</td>
    <td>1</td>
    <td>0</td>
  </tr>
  <tr>
  	<td>Default Value</td>
    <td>0</td>
    <td>0</td>
    <td>0</td>
    <td>0</td>
  </tr>
  <tr>
  	<td>Content</td>
    <td>reserved</td>
    <td>reserved</td>
    <td>reserved</td>
    <td>Gnss_en</td>
  </tr>
</table>

ble_transmit：‘1’使能数据传输

nb_transmit：‘1’使能NB/CAT1数据传输(暂不支持)

onoff ：‘1’开启传感器(若传感器未开启则会立即打开)

## 3. 蓝牙协议

### 3.1 传感器控制

#### 3.1.1 设置

APP下发：

<table>
  <tr>
  	<td></td>
    <td>数据</td>
    <td>长度</td>
    <td colspan="2">说明</td>
  </tr>
  <tr>
  	<td>包头</td>
    <td>0x68</td>
    <td>1</td>
    <td colspan="2"></td>
  </tr>
  <tr>
  	<td>数据长度</td>
    <td>0x3c</td>
    <td>1</td>
    <td colspan="2"></td>
  </tr>
  <tr>
  	<td>数据长度</td>
    <td>3+n</td>
    <td>2</td>
    <td colspan="2"></td>
  </tr>
  <tr>
  	<td rowspan="7">数据域</td>
    <td rowspan="7"></td>
    <td>1</td>
    <td colspan="2">0xFF(固定值)</td>
  </tr>
  <tr>
    <td>1</td>
    <td colspan="2">0x02(参数配置)</td>
  </tr>
  <tr>
    <td>1</td>
    <td colspan="2">0x01(设置)</td>
  </tr>
  <tr>
    <td rowspan="4">n</td>
    <td colspan="2">一次可以设置多个传感器参数</td>
  </tr>
  <tr>
    <td>2</td>
    <td>1B传感器类型 + 1B控制参数 (详细说明)</td>
  </tr>
  <tr>
    <td>2</td>
    <td>1B传感器类型 + 1B控制参数</td>
  </tr>
  <tr>
    <td>…</td>
    <td>…</td>
  </tr>
  <tr>
  	<td>校验码</td>
    <td>CS</td>
    <td>1</td>
    <td colspan="2">校验位</td>
  </tr>
  <tr>
  	<td>包尾</td>
    <td>0x16</td>
    <td></td>
    <td colspan="2"></td>
  </tr>
</table>

终端上传：

<table>
  <tr>
  	<td></td>
    <td>数据</td>
    <td>长度</td>
    <td colspan="2">说明</td>
  </tr>
  <tr>
  	<td>包头</td>
    <td>0x68</td>
    <td>1</td>
    <td colspan="2"></td>
  </tr>
  <tr>
  	<td>控制码</td>
    <td>0xbc</td>
    <td>1</td>
    <td colspan="2"></td>
  </tr>
  <tr>
  	<td>数据长度</td>
    <td>3+n</td>
    <td>2</td>
    <td colspan="2"></td>
  </tr>
  <tr>
  	<td rowspan="7">数据域</td>
    <td rowspan="7"></td>
    <td>1</td>
    <td colspan="2">0xFF(固定值)</td>
  </tr>
  <tr>
    <td>1</td>
    <td colspan="2">0x02(参数配置)</td>
  </tr>
  <tr>
    <td>1</td>
    <td colspan="2">0x01(设置)</td>
  </tr>
  <tr>
    <td rowspan="4">n</td>
    <td colspan="2">状态: 0x00 OK, Other error</td>
  </tr>
  <tr>
    <td>2</td>
    <td>1B类型 + 1B状态</td>
  </tr>
  <tr>
    <td>2</td>
    <td>1B类型 + 1B状态</td>
  </tr>
  <tr>
    <td>…</td>
    <td>…</td>
  </tr>
  <tr>
  	<td>校验码</td>
    <td>CS</td>
    <td>1</td>
    <td colspan="2">校验位</td>
  </tr>
  <tr>
  	<td>包尾</td>
    <td>0x16</td>
    <td></td>
    <td colspan="2"></td>
  </tr>
</table>
#### 3.1.2 读取

APP下发：

<table>
  <tr>
  	<td></td>
    <td>数据</td>
    <td>长度</td>
    <td colspan="2">说明</td>
  </tr>
  <tr>
  	<td>包头</td>
    <td>0x68</td>
    <td>1</td>
    <td colspan="2"></td>
  </tr>
  <tr>
  	<td>控制码</td>
    <td>0x3c</td>
    <td>1</td>
    <td colspan="2"></td>
  </tr>
  <tr>
  	<td>数据长度</td>
    <td>3+n</td>
    <td>2</td>
    <td colspan="2"></td>
  </tr>
  <tr>
  	<td rowspan="7">数据域</td>
    <td rowspan="7"></td>
    <td>1</td>
    <td colspan="2">0xFF(固定值)</td>
  </tr>
  <tr>
    <td>1</td>
    <td colspan="2">0x02(参数配置)</td>
  </tr>
  <tr>
    <td>1</td>
    <td colspan="2">0x02(读取)</td>
  </tr>
  <tr>
    <td rowspan="4">n</td>
  </tr>
  <tr>
    <td>1</td>
    <td>1B传感器类型</td>
  </tr>
  <tr>
    <td>1</td>
    <td>1B传感器类型</td>
  </tr>
  <tr>
    <td>…</td>
    <td>…</td>
  </tr>
  <tr>
  	<td>校验码</td>
    <td>CS</td>
    <td>1</td>
    <td colspan="2">校验位</td>
  </tr>
  <tr>
  	<td>包尾</td>
    <td>0x16</td>
    <td></td>
    <td colspan="2"></td>
  </tr>
</table



终端上传：

<table>
  <tr>
  	<td></td>
    <td>数据</td>
    <td>长度</td>
    <td colspan="2">说明</td>
  </tr>
  <tr>
  	<td>包头</td>
    <td>0x68</td>
    <td>1</td>
    <td colspan="2"></td>
  </tr>
  <tr>
  	<td>控制码</td>
    <td>0xbc</td>
    <td>1</td>
    <td colspan="2"></td>
  </tr>
  <tr>
  	<td>数据长度</td>
    <td>3+n</td>
    <td>2</td>
    <td colspan="2"></td>
  </tr>
  <tr>
  	<td rowspan="7">数据域</td>
    <td rowspan="7"></td>
    <td>1</td>
    <td colspan="2">0xFF(固定值)</td>
  </tr>
  <tr>
    <td>1</td>
    <td colspan="2">0x02(参数配置)</td>
  </tr>
  <tr>
    <td>1</td>
    <td colspan="2">0x02(读取)</td>
  </tr>
  <tr>
    <td rowspan="4">n</td>
  </tr>
  <tr>
    <td>2</td>
    <td>1B传感器类型 + 1B传感器参数 (详细说明)</td>
  </tr>
  <tr>
    <td>2</td>
    <td>1B传感器类型 + 1B传感器参数</td>
  </tr>
  <tr>
    <td>…</td>
    <td>…</td>
  </tr>
  <tr>
  	<td>校验码</td>
    <td>CS</td>
    <td>1</td>
    <td colspan="2">校验位</td>
  </tr>
</table

### 3.2 传感器使能

设备 **开始／结束** 传送原始数据的时候设备发送该指令到APP

终端上传：

<table>
  <tr>
  	<td></td>
    <td>数据</td>
    <td>长度</td>
    <td>说明</td>
  </tr>
  <tr>
  	<td>包头</td>
    <td>0x68</td>
    <td>1</td>
    <td></td>
  </tr>
  <tr>
  	<td>控制码</td>
    <td>0xbc</td>
    <td>1</td>
    <td></td>
  </tr>
  <tr>
  	<td>数据长度</td>
    <td>4</td>
    <td>2</td>
    <td></td>
  </tr>
  <tr>
  	<td rowspan="4">数据域</td>
    <td></td>
    <td>1</td>
    <td>0xFF(固定值)</td>
  </tr>
  <tr>
    <td></td>
    <td>1</td>
    <td>0x01(数据传输信号)</td>
  </tr>
  <tr>
    <td></td>
    <td>1</td>
    <td>传感器类型</td>
  </tr>
  <tr>
    <td></td>
    <td>1</td>
    <td>信号类型<br />
				0x01传输开始，0x02传输结束
</td>
  </tr>
  <tr>
  	<td>校验码</td>
    <td>CS</td>
    <td>1</td>
    <td>校验位</td>
  </tr>
  <tr>
  	<td>包尾</td>
    <td>0x16</td>
    <td></td>
    <td></td>
  </tr>
</table>

### 3.3 传感器数据传输

#### 3.3.1 PPG原始数据上传

Table 4 PPG数据参数表

<table>
  <tr>
  	<td>Name</td>
    <td colspan="4">Content</td>
  </tr>
  <tr>
  	<td>Bit</td>
    <td>7</td>
    <td>6</td>
    <td>5</td>
    <td>4</td>
  </tr>
  <tr>
  	<td>Default Value</td>
    <td>0</td>
    <td>0</td>
    <td>0</td>
    <td>0</td>
  </tr>
  <tr>
  	<td>Content</td>
    <td>reserved</td>
    <td>reserved</td>
    <td>reserved</td>
    <td>reserved</td>
  </tr>
  <tr>
  	<td>Bit</td>
    <td>3</td>
    <td>2</td>
    <td>1</td>
    <td>0</td>
  </tr>
  <tr>
  	<td>Default Value</td>
    <td>0</td>
    <td>0</td>
    <td>0</td>
    <td>0</td>
  </tr>
  <tr>
  	<td>Content</td>
    <td>reserved</td>
    <td>reserved</td>
    <td>reserved</td>
    <td>reserved</td>
  </tr>
</table>

终端上传：

<table>
  <tr>
  	<td></td>
    <td>数据</td>
    <td>长度</td>
    <td colspan="2">说明</td>
  </tr>
  <tr>
  	<td>包头</td>
    <td>0x68</td>
    <td>1</td>
    <td colspan="2"></td>
  </tr>
  <tr>
  	<td>控制码</td>
    <td>0xbc</td>
    <td>1</td>
    <td colspan="2"></td>
  </tr>
  <tr>
  	<td>数据长度</td>
    <td>3+n</td>
    <td>2</td>
    <td colspan="2"></td>
  </tr>
  <tr>
  	<td rowspan="7">数据域</td>
    <td rowspan="7"></td>
    <td>1</td>
    <td colspan="2">0x01(PPG传感器)</td>
  </tr>
  <tr>
    <td>1</td>
    <td colspan="2">PPG数据参数Table 4</td>
  </tr>
  <tr>
    <td>1</td>
    <td colspan="2">采样频率Hz</td>
  </tr>
  <tr>
    <td rowspan="4">n</td>
    <td colspan="2">一次上传包含多组PPG数据(原始值转换见Table 5)<br />
Green绿光， Red 红光， IR红外光
</td>
  </tr>
  <tr>
    <td>9</td>
    <td>3B Green + 3B Red + 3B IR </td>
  </tr>
  <tr>
    <td>9</td>
    <td>3B Green + 3B Red + 3B IR</td>
  </tr>
  <tr>
    <td>…</td>
    <td>…</td>
  </tr>
  <tr>
  	<td>校验码</td>
    <td>CS</td>
    <td>1</td>
    <td colspan="2">校验位</td>
  </tr>
  <tr>
  	<td>包尾</td>
    <td>0x16</td>
    <td></td>
    <td colspan="2"></td>
  </tr>
</table>

Table 5 PPG原始数据转换方法

```c
{
	(9B数据转换)
	Green(int) = (int)[1,3]
	Red(int)   = (int)[4,6]
	IR(int)    = (int)[7,9]
}

```

#### 3.3.2 ECG原始数据上传

Table 6 ECG数据参数表

<table>
  <tr>
  	<td>Name</td>
    <td colspan="4">Content</td>
  </tr>
  <tr>
  	<td>Bit</td>
    <td>7</td>
    <td>6</td>
    <td>5</td>
    <td>4</td>
  </tr>
  <tr>
  	<td>Default Value</td>
    <td>0</td>
    <td>0</td>
    <td>0</td>
    <td>0</td>
  </tr>
  <tr>
  	<td>Content</td>
    <td>reserved</td>
    <td>reserved</td>
    <td>reserved</td>
    <td>reserved</td>
  </tr>
  <tr>
  	<td>Bit</td>
    <td>3</td>
    <td>2</td>
    <td>1</td>
    <td>0</td>
  </tr>
  <tr>
  	<td>Default Value</td>
    <td>0</td>
    <td>0</td>
    <td>0</td>
    <td>0</td>
  </tr>
  <tr>
  	<td>Content</td>
    <td>reserved</td>
    <td>reserved</td>
    <td>reserved</td>
    <td>reserved</td>
  </tr>
</table>

终端上传：

<table>
  <tr>
  	<td></td>
    <td>数据</td>
    <td>长度</td>
    <td colspan="2">说明</td>
  </tr>
  <tr>
  	<td>包头</td>
    <td>0x68</td>
    <td>1</td>
    <td colspan="2"></td>
  </tr>
  <tr>
  	<td>控制码</td>
    <td>0xbc</td>
    <td>1</td>
    <td colspan="2"></td>
  </tr>
  <tr>
  	<td>数据长度</td>
    <td>3+n</td>
    <td>2</td>
    <td colspan="2"></td>
  </tr>
  <tr>
  	<td rowspan="7">数据域</td>
    <td rowspan="7"></td>
    <td>1</td>
    <td colspan="2">0x02(ECG传感器)</td>
  </tr>
  <tr>
    <td>1</td>
    <td colspan="2">ECG数据参数Table 6</td>
  </tr>
  <tr>
    <td>1</td>
    <td colspan="2">采样频率Hz</td>
  </tr>
  <tr>
    <td rowspan="4">n</td>
    <td colspan="2">一次上传包含多组ECG数据(原始值转换见Table 7)</td>
  </tr>
  <tr>
    <td>3</td>
    <td>3B ECG </td>
  </tr>
  <tr>
    <td>3</td>
    <td>3B ECG</td>
  </tr>
  <tr>
    <td>…</td>
    <td>…</td>
  </tr>
  <tr>
  	<td>校验码</td>
    <td>CS</td>
    <td>1</td>
    <td colspan="2">校验位</td>
  </tr>
  <tr>
  	<td>包尾</td>
    <td>0x16</td>
    <td></td>
    <td colspan="2"></td>
  </tr>
</table>

Table 7 ECG原始数据转换**:**

```c
{
    (将原始值转换成ADC值单位mv)
    int ecgVal;//为3B原始值
    int flag = ecgVal & 0x20000;

    if(flag != 0)
    {
        ecgVal = ecgVal - 262144;
    } 

    float mv = 1000 * (ecgVal) / (131072.0 * 20);//mv数据转换值
}

```

#### 3.3.3 IMU原始数据上传

Table 8 Gsensor数据参数表

<table>
  <tr>
  	<td>Name</td>
    <td colspan="4">Content</td>
  </tr>
  <tr>
  	<td>Bit</td>
    <td>7</td>
    <td>6</td>
    <td>5</td>
    <td>4</td>
  </tr>
  <tr>
  	<td>Default Value</td>
    <td>0</td>
    <td>0</td>
    <td>0</td>
    <td>0</td>
  </tr>
  <tr>
  	<td>Content</td>
    <td>transmit</td>
    <td>reserved</td>
    <td>reserved</td>
    <td>reserved</td>
  </tr>
  <tr>
  	<td>Bit</td>
    <td>3</td>
    <td>2</td>
    <td>1</td>
    <td>0</td>
  </tr>
  <tr>
  	<td>Default Value</td>
    <td>0</td>
    <td>0</td>
    <td>0</td>
    <td>0</td>
  </tr>
  <tr>
  	<td>Content</td>
    <td>reserved</td>
    <td>Mag_d</td>
    <td>Gyr_d</td>
    <td>Acc_d</td>
  </tr>
</table>

Mag_d:‘1’包含加速度数据

Gyr_d:‘1’包含陀螺仪数据

Acc_d:‘1’包含磁力计数据

终端上传：

<table>
  <tr>
  	<td></td>
    <td>数据</td>
    <td>长度</td>
    <td colspan="3">说明</td>
  </tr>
  <tr>
  	<td>包头</td>
    <td>0x68</td>
    <td>1</td>
    <td colspan="3"></td>
  </tr>
  <tr>
  	<td>控制码</td>
    <td>0xbc</td>
    <td>1</td>
    <td colspan="3"></td>
  </tr>
  <tr>
  	<td>数据长度</td>
    <td>2+N</td>
    <td>2</td>
    <td colspan="3"></td>
  </tr>
  <tr>
  	<td rowspan="18">数据域</td>
    <td rowspan="18"></td>
    <td>1</td>
    <td colspan="3">0x03(Gsensor传感器)</td>
  </tr>
  <tr>
    <td>1</td>
    <td colspan="3">Gsensor数据参数Table 8</td>
  </tr>
  <tr>
    <td>1</td>
    <td colspan="3">采样频率Hz</td>
  </tr>
  <tr>
    <td rowspan="4">n</td>
    <td colspan="3">
     一次上传包含多组Gsensor数据(原始值转换见Table 9)<br />
		6B数据格式: 2B x + 2B y + 2B z (xyz轴向)<br />
		优先级:ACC > GYRO > MAG<br />
		例1: 上传包含ACC与MAG时,为12B数据，<br />
		顺序为:6B ACC + 6B MAG<br />
		例2: 上传包含ACC,GYRO与MAG时,为18B数据，<br />
		顺序为:6B ACC + 6B GYRO + 6B MAG
    </td>
  </tr>
  <tr>
    <td>6/12/18</td>
    <td colspan="2">6B ACC + 6B GYRO + 6B MAG</td>
  </tr>
  <tr>
    <td>6/12/18</td>
    <td colspan="2">6B ACC + 6B GYRO + 6B MAG</td>
  </tr>
  <tr>
    <td>…</td>
    <td colspan="2">…</td>
  </tr>
  <tr>
    <td rowspan="10">n</td>
    <td>字节数(LSB)</td>
    <td>说明</td>
    <td>备注</td>
  </tr>
  <tr>
    <td>2</td>
    <td>Acc x</td>
    <td rowspan="3">加速度数据</td>
  </tr>
  <tr>
    <td>2</td>
    <td>Acc y</td>
  </tr>
  <tr>
    <td>2</td>
    <td>Acc z</td>
  </tr>
  <tr>
    <td>2</td>
    <td>Gyr x</td>
    <td rowspan="3">陀螺仪数据</td>
  </tr>
  <tr>
    <td>2</td>
    <td>Gyr y</td>
  </tr>
  <tr>
    <td>2</td>
    <td>Gyr z</td>
  </tr>
  <tr>
    <td>2</td>
    <td>Mag x</td>
    <td rowspan="3">磁力计数据</td>
  </tr>
  <tr>
    <td>2</td>
    <td>Mag y</td>
  </tr>
  <tr>
    <td>2</td>
    <td>Mag z</td>
  </tr>
  <tr>
    <td>…</td>
    <td colspan="3">…</td>
  </tr>
  <tr>
  	<td>校验码</td>
    <td>CS</td>
    <td>1</td>
    <td colspan="3">校验位</td>
  </tr>
  <tr>
  	<td>包尾</td>
    <td>0x16</td>
    <td></td>
    <td colspan="3"></td>
  </tr>
</table>

Table 9 Gsensor原始数据转换**:**

```c
< 设备B10C >
6B ACC转换重力速度值
{
  int16_t x_raw,y_raw,z_raw; //x_raw,y_raw,z_raw为2B原始值
  float g = 9.80; //重力加速度值
  float x = (x_raw * 16 / 32767) * g;
  float y = (y_raw * 16 / 32767) * g;
  float z = (z_raw * 16 / 32767) * g;
}
6B GYRO转换弧度值
{
  int16_t x_raw,y_raw,z_raw; //x_raw,y_raw,z_raw为2B原始值
  float rad = 3.14 / 180; 
  float x = (x_raw * 2000 / 32767) * rad;
  float y = (y_raw * 2000 / 32767) * rad;
  float z = (z_raw * 2000 / 32767) * rad;
}

```

#### 3.3.4 GNSS原始数据上传

<table>
  <tr>
  	<td></td>
    <td>数据</td>
    <td>长度</td>
    <td>说明</td>
  </tr>
  <tr>
  	<td>包头</td>
    <td>0x68</td>
    <td>1</td>
    <td></td>
  </tr>
  <tr>
  	<td>控制码</td>
    <td>0xbc</td>
    <td>1</td>
    <td></td>
  </tr>
  <tr>
  	<td>数据长度</td>
    <td>2+N</td>
    <td>2</td>
    <td></td>
  </tr>
  <tr>
  	<td rowspan="6">数据域</td>
    <td rowspan="6"></td>
    <td>1</td>
    <td>0x05(Gnss传感器)</td>
  </tr>
  <tr>
    <td>1</td>
    <td>Gnss数据参数</td>
  </tr>
  <tr>
    <td>1</td>
    <td>采样频率Hz (保留 0)</td>
  </tr>
  <tr>
    <td>1</td>
    <td>总包数(默认1，当一次无法发送完成时为 > 1的值)</td>
  </tr>
  <tr>
    <td>1</td>
    <td>索引值(起始值 1)</td>
  </tr>
  <tr>
    <td>xx</td>
    <td>Gnss 原始数据(Ascll),以 \r\n 表示一段数据结尾</td>
  </tr>
  <tr>
  	<td>校验码</td>
    <td>CS</td>
    <td>1</td>
    <td>校验位</td>
  </tr>
  <tr>
  	<td>包尾</td>
    <td>0x16</td>
    <td></td>
    <td></td>
  </tr>
</table>

Table 10 Gnss数据参数表

<table>
  <tr>
  	<td>Name</td>
    <td colspan="4">Content</td>
  </tr>
  <tr>
  	<td>Bit</td>
    <td>7</td>
    <td>6</td>
    <td>5</td>
    <td>4</td>
  </tr>
  <tr>
  	<td>Default Value</td>
    <td>0</td>
    <td>0</td>
    <td>0</td>
    <td>0</td>
  </tr>
  <tr>
  	<td>Content</td>
    <td>reserved</td>
    <td>reserved</td>
    <td>reserved</td>
    <td>reserved</td>
  </tr>
  <tr>
  	<td>Bit</td>
    <td>3</td>
    <td>2</td>
    <td>1</td>
    <td>0</td>
  </tr>
  <tr>
  	<td>Default Value</td>
    <td>0</td>
    <td>0</td>
    <td>0</td>
    <td>0</td>
  </tr>
  <tr>
  	<td>Content</td>
    <td>reserved</td>
    <td>reserved</td>
    <td>reserved</td>
    <td>reserved</td>
  </tr>
</table>

## 4. 演示例程

### 4.1 说明

**注：不建议同时开启多个原始数据功能，数据量过大容易造成数据溢出丢失**

**主动方式**

用户主动开启传感器，以获取实时传感器数据

**监听方式**

用于抓取全天监测时间段的各传感器原始数据，可便于算法更新迭代，或其他需求

### 4.2 PPG原始数据获取

**主动方式**

开启：

| **发送****(Hex)**                 | **接收****(Hex)**                | **说明**                                                   |
| --------------------------------- | -------------------------------- | ---------------------------------------------------------- |
| 68 3C 05 00 FF 02  01 01 83 2E 16 | 68 BC 05 00 FF 02 01 01 00 2C 16 | 打开PPG(Green LED)，  开启蓝牙数据传输                     |
|                                   | 68 BC 04 00 FF 01 01 01 2A  16   | 收到PPG数据传输开始信号  (开始上传数据)                    |
|                                   | 68 BC XX XX 01 00 XX XX ~ XX 16  | 接收上传数据  (首次开启可能需要等待30秒左右才会有数据上传) |
|                                   | . . .                            |                                                            |

关闭：

| **发送****(Hex)**                 | **接收****(Hex)**                | **说明**                            |
| --------------------------------- | -------------------------------- | ----------------------------------- |
| 68 3C 05 00 FF 02  01 01 00 AC 16 | 68 BC 05 00 FF 02 01 01 00 2C 16 | 关闭PPG原始数据功能，  关闭数据传输 |

**监听方式**

开启：

| **发送****(Hex)**                | **接收****(Hex)**                 | **说明**                                |
| -------------------------------- | --------------------------------- | --------------------------------------- |
| 68 3C 05 00 FF 02 01 01 80 2C 16 | 68 BC 05 00 FF  02 01 01 00 2C 16 | 开启蓝牙数据传输  (开始监听)            |
|                                  | 68 BC 04 00 FF 01 01 01 2A  16    | 收到PPG数据传输开始信号  (开始上传数据) |
|                                  | 68 BC XX XX 01 00 XX XX ~ XX 16   | 接收上传数据                            |
|                                  | . . .                             |                                         |
|                                  | 68 BC 04 00 FF 01 01 02 2B 16     | 收到PPG数据传输停止信号  (数据上传完成) |

关闭：

| **发送****(Hex)**                 | **接收****(Hex)**                | **说明**                 |
| --------------------------------- | -------------------------------- | ------------------------ |
| 68 3C 05 00 FF 02  01 01 00 AC 16 | 68 BC 05 00 FF 02 01 01 00 2C 16 | 关闭数据传输  (停止监听) |

### 4.3 ECG原始数据获取

**主动方式**

开启：

| **发送****(Hex)**                 | **接收****(Hex)**                | **说明**                                |
| --------------------------------- | -------------------------------- | --------------------------------------- |
| 68 3C 05 00 FF 02  01 02 81 2E 16 | 68 BC 05 00 FF 02 01 02 00 2D 16 | 打开ECG，  开启蓝牙数据传输             |
|                                   | 68 BC 04 00 FF 01 02 01 2B  16   | 收到ECG数据传输开始信号  (开始上传数据) |
|                                   | 68 BC XX XX 02 00 XX XX ~ XX 16  | 接收上传数据                            |
|                                   | . . .                            |                                         |

 关闭：

| **发送****(Hex)**                 | **接收****(Hex)**                | **说明**                |
| --------------------------------- | -------------------------------- | ----------------------- |
| 68 3C 05 00 FF 02  01 02 00 AD 16 | 68 BC 05 00 FF 02 01 02 00 2D 16 | 关闭ECG，  关闭数据传输 |

**监听方式**

开启

| **发送****(Hex)**                | **接收****(Hex)**                 | **说明**                                |
| -------------------------------- | --------------------------------- | --------------------------------------- |
| 68 3C 05 00 FF 02 01 02 80 2D 16 | 68 BC 05 00 FF  02 01 02 00 2D 16 | 开启蓝牙数据传输   (开始监听)           |
|                                  | 68 BC 04 00 FF 01 02 01 2B  16    | 收到ECG数据传输开始信号  (开始上传数据) |
|                                  | 68 BC XX XX 02 00 XX XX ~ XX 16   | 接收上传数据                            |
|                                  | . . .                             |                                         |
|                                  | 68 BC 04 00 FF 01 02 02 2C 16     | 收到ECG数据传输停止信号  (数据上传完成) |

 

关闭ECG原始数据功能

| **发送****(Hex)**                 | **接收****(Hex)**                | **说明**                  |
| --------------------------------- | -------------------------------- | ------------------------- |
| 68 3C 05 00 FF 02  01 02 00 2D 16 | 68 BC 05 00 FF 02 01 02 00 2D 16 | 关闭数据传输   (停止监听) |

### 4.4 IMU原始数据获取

**主动方式**

开启：

| **发送****(Hex)**                 | **接收****(Hex)**                | **说明**                           |
| --------------------------------- | -------------------------------- | ---------------------------------- |
| 68 3C 05 00 FF 02  01 03 87 35 16 | 68 BC 05 00 FF 02 01 03 00 2E 16 | 打开ACC、GYR，  开启蓝牙数据传输   |
|                                   | 68 BC 04 00 FF 01 03 01 2C  16   | 收到数据传输开始信号(开始上传数据) |
|                                   | 68 BC XX XX 03 XX XX ~ XX 16     | 接收上传数据                       |
|                                   | . . .                            |                                    |

关闭：

| **发送****(Hex)**                 | **接收****(Hex)**                | **说明**                     |
| --------------------------------- | -------------------------------- | ---------------------------- |
| 68 3C 05 00 FF 02  01 03 00 AE 16 | 68 BC 05 00 FF 02 01 03 00 2E 16 | 关闭ACC、GYR，  关闭数据传输 |

**监听方式**

开启：

| **发送****(Hex)**                | **接收****(Hex)**                 | **说明**                           |
| -------------------------------- | --------------------------------- | ---------------------------------- |
| 68 3C 05 00 FF 02 01 03 80 35 16 | 68 BC 05 00 FF  02 01 03 00 2E 16 | 开启蓝牙数据传输   (开始监听)      |
|                                  | 68 BC 04 00 FF 01 03 01 2C  16    | 收到数据传输开始信号(开始上传数据) |
|                                  | 68 BC XX XX 03 XX XX ~ XX 16      | 接收上传数据                       |
|                                  | . . .                             |                                    |
|                                  | 68 BC 04 00 FF 01 03 02 2D 16     | 收到数据传输结束信号(数据上传完成) |

 关闭：

| **发送****(Hex)**                 | **接收****(Hex)**                | **说明**                  |
| --------------------------------- | -------------------------------- | ------------------------- |
| 68 3C 05 00 FF 02  01 03 00 AE 16 | 68 BC 05 00 FF 02 01 03 00 2E 16 | 关闭数据传输   (停止监听) |



## 5. NB/CAT1协议

### 5.1 数据缓存

1. ppg数据 每分钟100HZ\*9*60 = 54000 
2. ECG数据 每分钟250HZ\*3*60 = 45000
3. Gsensor数据 每分钟100HZ\*12*60 = 72000
4. GNSS原始数据[跟蓝牙协议不同，这里存储定位数据，用于运动轨迹上传]每分钟 1HZ\*15*60 = 900
5. 运动生理原始数据 每分钟12*10 每小时 120\*6
6. 1分钟所有数据 135000 最小擦除扇区大小4096字节，需要33扇区
7. 10分钟所有数据1350000，需要330个扇区

### 5.2 参数设置/读取协议[json格式]

#### 5.2.1 系统下发

| 键值          | 数据类型 | 说明                                                         |
| ------------- | -------- | ------------------------------------------------------------ |
| rawdataConfig | string   | query/set                                                    |
| ppg           | string   | 转换为uint8参考蓝牙协议控制参数[ble_transmit无效]            |
| ecg           | string   | 转换为uint8参考蓝牙协议控制参数[ble_transmit无效]            |
| gsensor       | string   | 转换为uint8参考蓝牙协议控制参数[ble_transmit无效]            |
| location      | string   | 转换为uint8参考蓝牙协议控制参数[ble_transmit无效],上报数据内容与蓝牙协议不同 |
| flags         | string   | 转换为uint32<br>附加功能<br>0x00000001：初始化所有缓存<br>0x00000002：重置所有采集<br/>0x00000004：定时采集 |
| times         | string   | 转换为uint32<br>定时采集的时候使用，定时采集多少s后关闭      |

#### 5.2.2 终端回复

| 键值             | 数据类型 | 说明                                                         |
| ---------------- | -------- | ------------------------------------------------------------ |
| ackRawdataConfig | int      | 1成功 0失败                                                  |
| ppg              | string   | 转换为uint8参考蓝牙协议控制参数[ble_transmit无效]            |
| ecg              | string   | 转换为uint8参考蓝牙协议控制参数[ble_transmit无效]            |
| gsensor          | string   | 转换为uint8参考蓝牙协议控制参数[ble_transmit无效]            |
| location         | string   | 转换为uint8参考蓝牙协议控制参数[ble_transmit无效],上报数据内容与蓝牙协议不同 |
| flags            | string   | 转换为uint32<br>附加功能<br>0x00000001：初始化所有缓存<br>0x00000002：重置所有采集<br/>0x00000004：定时采集 |
| times            | string   | 转换为uint32<br>定时采集的时候使用，定时采集多少s后关闭      |

### 5.3 数据传输协议

每次传输一个扇区

| 包头       | 包头1B              | 0x68                                                         |
| ---------- | ------------------- | ------------------------------------------------------------ |
| HEAD16B+2B | 原始数据类型1B      | [2.2指令／数据类型表](#_2.2 指令／数据类型表)                |
|            | 每组数据大小1B      | 不同原始数据类型不一样PPG,ECG,Gsensor数据结构，大小参考本文档蓝牙协议GNSS数据结构参考文档《NB接口说明书_v2.17_20220124》1.4.7表格 66定位数据格式 |
|            | 总数据组数2B        | 该扇区存储数据组总数                                         |
|            | 数据缓存时间4B      | 本扇区存储数据时间                                           |
|            | 采集开始/结束时间4B | 开始结束标记为0x01的时候为采集开始时间开始结束标记为0x02的时候为采集结束时间开始结束标记为0x00的时候忽略此位置 |
|            | 开始结束标记1B      | 0x01开始信号0x02结束信号0x03数据传输中                       |
|            | 频率1B              | 数据采集频率                                                 |
|            | 数据控制参数1B      | 参考蓝牙协议数据参数                                         |
|            | 备用 1B             |                                                              |
|            | 备用 1B             |                                                              |
|            | CRC8校验            |                                                              |
| DATA1      | 本组数据长度1B      | 数据+校验位长度                                              |
|            | 数据nB              | PPG：必须是9的倍数ECG：必须是3的倍数Gsensor：必须是          |
|            | 备用1B              |                                                              |
|            | 校验位              | CRC8校验                                                     |
| DATA2      | 同DATA1             |                                                              |
| ......     |                     |                                                              |
| 包尾       | 包尾1B              | 0x16                                                         |







