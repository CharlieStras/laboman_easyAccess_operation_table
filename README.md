# easyAccess流水线操作记录
## 记录明细
|序号|名称|内容|最大容量|备注|
|---|---|---|---|---|
|1|时间|YYYYMMDDHHMMSS|14|操作记录的时间|
|2|标本号|Sample ID number|22||
|3|记录源|Analyzer name^<br>Inquiry type^<br>Inquiry unit number|15^<br>2<br>2|Inquiry type包含如下四种<br>B: BT指令询问<br>C: 非BT(CVR)指令询问<br>SI: 进TS-10时指令询问<br>SO: 出TS-10时指令询问|
|4|记录源序列号|Analyzer serial No.|15||
|5|记录类型|0, 1, 2, Q, O, R|1|"0": 接收LIS指令<br>"1": 接收标本的病人信息<br>"2": 发送标本的检验结果给LIS<br>"Q": 接收仪器的指令询问<br>"O": 发送标本的指令给仪器<br>"R": 接收仪器的检验结果|
|6|管架号|Rack No.|6||
|7|位置号|Rack Position|2||
|8|仪器记录的时间|YYYYMMDDHHMMSS|14|仪器原始记录中的时间|
|9|检验指令|Order type^<br>Parameters|100|指令类别如下<br>"A": Laboman检验申请的指令<br>"D": 默认指令<br>"E": 默认管架指令<br>"L": LIS指令<br>"R": 3R指令<br>"S": 共享指令<br><br>各检验项目用"+"分隔，如"CBC+DIFF+RET"|
|10|归档指令|Archiving instruction|2|CT90通讯程序发送的归档指令|
|11|归档结果|Archiving result|50|CT90通讯程序接收的归档结果，如:<br>FINAL^00^0377^OK^OK^OK<br>STORE-F^1^2^125^000171^124^1^OK|
|12|归档原因|Archiving reason|100|Laboman依照TS-10区域设置判定的归档原因或者误码等导致CT-90自定归档区域的原因|
|13|LIS短号|LIS No.|22||
## 示例
- 接收到CT90(无TS-10)的BT指令询问  
  20191208093420|              42000001|CT-90^B^01|00001|Q|000042|01|20191208093419||||42
