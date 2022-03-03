# ESP-S3-EYE 示例说明

## 交互系统

### 语音

语音交互逻辑遵循“先说唤醒词，再说命令词”。



### 按键

#### 

## 工作模式

该示例共包含四个工作模式：“待机模式”、“实时显示”、“人脸识别”和“移动侦测”。下面对这四个模式做简要介绍。

### 待机模式

待机模式下，LCD 屏幕上仅显示 Espressif Logo。该模式也是开发板上电以后的默认模式。

### 实时显示

实时显示模式下，LCD 屏幕上会实时显示摄像头采集的图片。

### 人脸识别

人脸识别模式下，LCD 屏幕上会实时显示摄像头采集的图片。并且实时检测画面中的人脸，并显示检测框和关键点。通过按键和语音交互可以实现人脸识别相关的操作，详见下表：

|   操作   |                     说明                     | 按键触发 |                语音触发                |
| :------: | :------------------------------------------: | :------: | :------------------------------------: |
| 识别人脸 |     识别当前画面中的人脸，并显示识别结果     |  “PLAY”  | “Hi，乐鑫”唤醒后，说出命令词“识别一下” |
| 添加人脸 |   添加当前画面中的人脸，并显示添加的 ID 号   |   “UP”   | “Hi，乐鑫”唤醒后，说出命令词“添加人脸” |
| 删除人脸 | 删除人脸库中的最后一个 ID， 并显示剩余 ID 数 |  “DOWN”  | “Hi，乐鑫”唤醒后，说出命令词“删除人脸” |

### 移动侦测

移动侦测模式下，LCD 屏幕上会实时显示摄像头采集的图片。并且实时检测画面中是否出现物体移动，如果物体移动，画面左上角会显示蓝点。



#### 进入默认固件
上电后等待3秒，不对开发板做任何操作，当LCD屏幕显示Espressif LOGO表示已进入默认固件。

#### 默认固件模式
默认固件存在四种运行模式，固件会默认先进入人脸识别模式：
1. 待机模式：该模式下开发板只有LCD工作，显示公司LOGO。
2. 实时显示模式：该模式下LCD会实时显示摄像头拍摄到的画面。
3. 人脸识别模式：该模式下LCD会实时显示摄像头拍摄到的画面，如果画面中存在人脸，LCD显示的画面上会框出人脸，并画出人脸的五个特征点。该模式下提供三种功能：录入人脸、识别人脸、删除人脸。
   - 录入人脸： 按下MENU键。或者使用“Hi，乐鑫”唤醒词唤醒，唤醒后摄像头旁的LED会被点亮，随后说出“添加人脸”。
   - 识别人脸： 按下UP键。或者使用“Hi，乐鑫”唤醒词唤醒，唤醒后摄像头旁的LED会被点亮，随后说出“识别一下”。
   - 删除人脸： 按下PLAY键。或者使用“Hi，乐鑫”唤醒词唤醒，唤醒后摄像头旁的LED会被点亮，随后说出“删除人脸”。
4. 移动侦测模式： 该模式下LCD会实时显示摄像头拍摄到的画面。若画面中存在物体移动，LCD中左上角会显示蓝色色块。

#### 模式切换
在任何时候都可以使用“Hi，乐鑫”唤醒词唤醒开发板，四种模式分别对应四个命令词。说出相应的命令词，识别成功后随即切换到对应的模式。工作模式与命令词的对应关系如下：
1. 待机模式：“停止工作”
2. 实时显示模式：“仅显示”
3. 人脸识别模式：“人脸识别”
4. 移动侦测模式：“移动侦测”

#### 语音系统
- 语音唤醒：默认固件工作时，任何时刻都可以使用“Hi，乐鑫”唤醒词唤醒开发板。开发板被唤醒后，摄像头旁的LED会常亮。
- 命令词识别：唤醒后会等待用户说出命令词。若识别成功，摄像头旁的LED会从常亮变为闪烁一秒, LED会随后熄灭。