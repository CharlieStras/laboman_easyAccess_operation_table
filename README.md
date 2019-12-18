# easyAccess流水线操作记录
## 记录明细
|序号|名称|内容|最大容量|备注|
|---|---|---|---|---|
|1|时间|YYYYMMDDHHMMSS|14|操作记录的时间|
|2|标本号|Sample ID number|22||
|3|记录源|Analyzer name^<br>Inquiry type^<br>Inquiry unit number|15^<br>2<br>2|Inquiry type包含如下四种<br>B: BT指令询问<br>C: 非BT(CVR)指令询问<br>SI: 进TS-10时指令询问<br>SO: 出TS-10时指令询问|
|4|记录源序列号|Analyzer serial No.|15||
|5|记录类型|0,1,2,Q,O,R|1|"0": 接收LIS指令<br>"1": 接收标本的病人信息<br>"2": 发送标本的检验结果给LIS<br>"Q": 接收仪器的指令询问<br>"O": 发送标本的指令给仪器<br>"R": 接收仪器的检验结果|
|6|管架号|Rack No.|6||
|7|位置号|Rack Position|2||
|8|仪器记录的时间|YYYYMMDDHHMMSS|14|仪器原始记录中的时间|
|9|LIS短号|LIS No.|22||
## 示例
- 接收到CT90(无TS-10)的BT指令询问  
  20191208093420|              42000001|CT-90_REC^B^01|00001|Q|000042|01|20191208093419|42
