# own-tinypxeserver

## LICENSE

[LICENSE | Github](LICENSE)

## DOT

```plain
PS C:\Users\Administrator\Downloads> echo @'
echo ""
echo "## Part 0"
echo ""

echo ""
echo "### Point 0.0.22"
echo ""

echo "[Node_0_ISP_Modem_0\nChina Telecom\nGPON / Bridge\nDown is Node_1_Switch_0] [Node_1_Switch_0\nUp is Node_0_ISP_Modem_0\nDown is Node_2_Switch_Central\n/ Node_3_Router_NorthWest] [Node_2_Switch_Central\nUp is Node_1_Switch_0\nDown is Node_4_Router_0] [Node_3_Router_NorthWest\nPPPoE\nUp is Node_1_Switch_0] [Node_4_Router_0\nPPPoE\n/ CIDR is 172.16.0.0/12\nUp is Node_2_Switch_Central\nDown is Node_5_Switch_0] [Node_5_Switch_0\nUp is Node_4_Router_0\nDown is Node_6_Wireless_Router_0\nDown is Node_7_Wireless_Router_1] [Node_6_Wireless_Router_0\nWire Repeater\n/ Extender\nUp is Node_5_Switch_0] [Node_7_Wireless_Router_1\nCIDR is 192.168.1.0/24\nUp is Node_5_Switch_0]" | graph-easy

echo ""
echo "### Point 0.1.19"
echo ""

$Node_0_ISP_Modem_0 = '[Node_0_ISP_Modem_0\nChina Telecom\nGPON / Bridge]'
$Node_1_Switch_0 = '[Node_1_Switch_0]'
$Node_2_Switch_Central = '[Node_2_Switch_Central]'
$Node_3_Router_NorthWest = '[Node_3_Router_NorthWest\nPPPoE]'
$Node_4_Router_0 = '[Node_4_Router_0\nPPPoE\n/ CIDR is 172.16.0.0/12]'
$Node_5_Switch_0 = '[Node_5_Switch_0]'
$Node_6_Wireless_Router_0 = '[Node_6_Wireless_Router_0\nWire Repeater\n/ Extender]'
$Node_7_Wireless_Router_1 = '[Node_7_Wireless_Router_1\nCIDR is 192.168.1.0/24]'

echo "$Node_0_ISP_Modem_0 -> $Node_1_Switch_0 $Node_1_Switch_0 -> $Node_2_Switch_Central $Node_1_Switch_0 -> $Node_3_Router_NorthWest $Node_2_Switch_Central -> $Node_4_Router_0 $Node_4_Router_0 -> $Node_5_Switch_0 $Node_5_Switch_0 -> $Node_6_Wireless_Router_0 $Node_5_Switch_0 -> $Node_7_Wireless_Router_1" | graph-easy
'@ > dot.ps1
PS C:\Users\Administrator\Downloads>
PS C:\Users\Administrator\Downloads> .\dot.ps1

## Part 0


### Point 0.0.22

+----------------------------------+
|        Node_0_ISP_Modem_0        |
|          China Telecom           |
|          GPON / Bridge           |
|     Down is Node_1_Switch_0      |
+----------------------------------+
+----------------------------------+
|         Node_1_Switch_0          |
|     Up is Node_0_ISP_Modem_0     |
|  Down is Node_2_Switch_Central   |
|    / Node_3_Router_NorthWest     |
+----------------------------------+
+----------------------------------+
|      Node_2_Switch_Central       |
|      Up is Node_1_Switch_0       |
|     Down is Node_4_Router_0      |
+----------------------------------+
+----------------------------------+
|     Node_3_Router_NorthWest      |
|              PPPoE               |
|      Up is Node_1_Switch_0       |
+----------------------------------+
+----------------------------------+
|         Node_4_Router_0          |
|              PPPoE               |
|     / CIDR is 172.16.0.0/12      |
|   Up is Node_2_Switch_Central    |
|     Down is Node_5_Switch_0      |
+----------------------------------+
+----------------------------------+
|         Node_5_Switch_0          |
|      Up is Node_4_Router_0       |
| Down is Node_6_Wireless_Router_0 |
| Down is Node_7_Wireless_Router_1 |
+----------------------------------+
+----------------------------------+
|     Node_6_Wireless_Router_0     |
|          Wire Repeater           |
|            / Extender            |
|      Up is Node_5_Switch_0       |
+----------------------------------+
+----------------------------------+
|     Node_7_Wireless_Router_1     |
|      CIDR is 192.168.1.0/24      |
|      Up is Node_5_Switch_0       |
+----------------------------------+

### Point 0.1.19

+--------------------+     +-------------------------+     +-----------------------+     +-------------------------+     +--------------------------+     +--------------------------+
| Node_0_ISP_Modem_0 |     |                         |     |                       |     |     Node_4_Router_0     |     |                          |     | Node_6_Wireless_Router_0 |
|   China Telecom    |     |     Node_1_Switch_0     |     | Node_2_Switch_Central |     |          PPPoE          |     |     Node_5_Switch_0      |     |      Wire Repeater       |
|   GPON / Bridge    | --> |                         | --> |                       | --> | / CIDR is 172.16.0.0/12 | --> |                          | --> |        / Extender        |
+--------------------+     +-------------------------+     +-----------------------+     +-------------------------+     +--------------------------+     +--------------------------+
                             |                                                                                             |
                             |                                                                                             |
                             v                                                                                             v
                           +-------------------------+                                                                   +--------------------------+
                           | Node_3_Router_NorthWest |                                                                   | Node_7_Wireless_Router_1 |
                           |          PPPoE          |                                                                   |  CIDR is 192.168.1.0/24  |
                           +-------------------------+                                                                   +--------------------------+
```

## DOT

```plain
PS C:\Users\Administrator\Downloads> echo @'
echo ""
echo "## Part 0"
echo ""

echo ""
echo "### Point 0.0.12"
echo ""

echo "[Node_0_Consumer_0] [Node_1_Consumer_Index] [Node_2_Consumer_Identity_Number] [Node_3_Consumer_Identity_Name] [Node_4_Consumer_Online_Time] [Node_5_Producer_Menu] [Node_6_Producer_Menu_Index] [Node_7_Producer_Menu_Project_Name] [Node_8_Producer_Menu_Count]" | graph-easy

echo ""
echo "### Point 0.1.14"
echo ""

$Node_0_Consumer_0 = '[Node_0_Consumer_0]'
$Node_1_Consumer_Index = '[Node_1_Consumer_Index]'
$Node_2_Consumer_Identity_Number = '[Node_2_Consumer_Identity_Number]'
$Node_3_Consumer_Identity_Name = '[Node_3_Consumer_Identity_Name]'
$Node_4_Consumer_Online_Time = '[Node_4_Consumer_Online_Time]'
$Node_5_Producer_Menu = '[Node_5_Producer_Menu]'
$Node_6_Producer_Menu_Index = '[Node_6_Producer_Menu_Index]'
$Node_7_Producer_Menu_Project_Name = '[Node_7_Producer_Menu_Project_Name]'
$Node_8_Producer_Menu_Count = '[Node_8_Producer_Menu_Count]'

echo "$Node_0_Consumer_0 -> $Node_1_Consumer_Index $Node_0_Consumer_0 -> $Node_2_Consumer_Identity_Number $Node_0_Consumer_0 -> $Node_3_Consumer_Identity_Name $Node_0_Consumer_0 -> $Node_4_Consumer_Online_Time $Node_0_Consumer_0 -> $Node_6_Producer_Menu_Index" | graph-easy

echo ""
echo "### Point 0.2.8"
echo ""

echo "$Node_5_Producer_Menu -> $Node_6_Producer_Menu_Index $Node_5_Producer_Menu -> $Node_7_Producer_Menu_Project_Name $Node_5_Producer_Menu -> $Node_8_Producer_Menu_Count" | graph-easy
'@ > dot.ps1
PS C:\Users\Administrator\Downloads>
PS C:\Users\Administrator\Downloads> .\dot.ps1

## Part 0


### Point 0.0.12

+-----------------------------------+
|         Node_0_Consumer_0         |
+-----------------------------------+
+-----------------------------------+
|       Node_1_Consumer_Index       |
+-----------------------------------+
+-----------------------------------+
|  Node_2_Consumer_Identity_Number  |
+-----------------------------------+
+-----------------------------------+
|   Node_3_Consumer_Identity_Name   |
+-----------------------------------+
+-----------------------------------+
|    Node_4_Consumer_Online_Time    |
+-----------------------------------+
+-----------------------------------+
|       Node_5_Producer_Menu        |
+-----------------------------------+
+-----------------------------------+
|    Node_6_Producer_Menu_Index     |
+-----------------------------------+
+-----------------------------------+
| Node_7_Producer_Menu_Project_Name |
+-----------------------------------+
+-----------------------------------+
|    Node_8_Producer_Menu_Count     |
+-----------------------------------+

### Point 0.1.14

+-----------------------------+     +-------------------------------+     +---------------------------------+
| Node_4_Consumer_Online_Time | <-- |                               | --> |      Node_1_Consumer_Index      |
+-----------------------------+     |       Node_0_Consumer_0       |     +---------------------------------+
+-----------------------------+     |                               |     +---------------------------------+
| Node_6_Producer_Menu_Index  | <-- |                               | --> | Node_2_Consumer_Identity_Number |
+-----------------------------+     +-------------------------------+     +---------------------------------+
                                      |
                                      |
                                      v
                                    +-------------------------------+
                                    | Node_3_Consumer_Identity_Name |
                                    +-------------------------------+

### Point 0.2.8

+----------------------------+     +-----------------------------------+     +----------------------------+
| Node_8_Producer_Menu_Count | <-- |       Node_5_Producer_Menu        | --> | Node_6_Producer_Menu_Index |
+----------------------------+     +-----------------------------------+     +----------------------------+
                                     |
                                     |
                                     v
                                   +-----------------------------------+
                                   | Node_7_Producer_Menu_Project_Name |
                                   +-----------------------------------+
```

```plain
PS C:\Users\Administrator\Downloads> echo @'
create database if not exists dot;

## 创建 consumer_0

use dot;

drop table if exists consumer_0;

create table consumer_0(
  consumerIndex INT auto_increment not null,
	consumerIdentityNumber VARCHAR(20),
	consumerIdentityName VARCHAR(10),
	consumerOnlineTime DATETIME,
	producerMenuIndex INT,
	PRIMARY KEY(consumerIndex),
	FOREIGN KEY(producerMenuIndex) REFERENCES producer_menu(producerMenuIndex)
);

## 为 consumer_0 增加 数据

insert into consumer_0 values (0, '210202199702194932', '唐铭泽', '2023-06-12 06:12:00', 0);

## 创建 producer_menu

use dot;

drop table if exists producer_menu;

create table producer_menu(
  producerMenuIndex INT auto_increment not null,
	producerMenuProjectName VARCHAR(20),
	producerMenuCount INT,
	PRIMARY KEY(producerMenuIndex)
);

## 为 producer_menu 增加 数据

insert into producer_menu values (0, '8 小时 畅玩', 8);
'@ > dot.sql
```