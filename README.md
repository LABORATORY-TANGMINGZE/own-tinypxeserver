# own-tinypxeserver

## LICENSE

[LICENSE | Github](LICENSE)

## DOT

```plain
PS C:\Users\ecs-user\Downloads> echo @'
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
PS C:\Users\ecs-user\Downloads>
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