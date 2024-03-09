\#include <iostream>
\#include <string>

using namespace std;

int main() {
cout << "此程序为应急时使用，使用前请自觉查阅丢失东西当天黄历以及丢失东西时的时辰"<< endl;
cout << "时辰参考：23点——1点 ——子时,1点——3点——丑时,3点——5点——寅时,5点——7点——卯时,7点——9点——辰时,9点——11点——巳时,11点——13点——午时,13点——15点——未时,15点——17点——申时,17点——19点——酉时,19点——21点——戌时,21点——23点——亥时"<< endl;
cout << "请输入日期(甲/乙/丙/丁/戊/己/庚/壬/癸)："<< endl;
string day;
cin >> day;

string position;
if (day == "甲") {
position = "正东方（震卦.伤门）";
} else if (day == "乙") {
position = "正南方（离卦.景门）";
} else if (day == "丙" || day == "辛") {
position = "西南方（坤卦.死门）";
} else if (day == "丁") {
position = "西北方（乾卦.开门）";
} else if (day == "戊") {
position = "北方（坎卦.休门）";
} else if (day == "己") {
position = "东南方（巽卦.杜门）";
} else if (day == "庚") {
position = "正西方（兑卦.惊）";
} else if (day == "壬" || day == "癸") {
position = "东北方（艮卦.生门）";
} else {
cout << "输入的日期无效" << endl;
return 0;
}

string owner;
if (day == "甲" || day == "己") {
owner = "男人手上";
} else if (day == "乙" || day == "庚") {
owner = "女人手上";
} else if (day == "丙" || day == "辛") {
owner = "小孩子手上";
} else if (day == "丁" || day == "壬") {
owner = "亲人手上";
} else if (day == "戊" || day == "癸") {
owner = "家中某处";
}

string time;
cout << "请输入时间(子/午/卯/酉/寅/申/巳/亥/辰/戌/丑/未)：";
cin >> time;

string range;
if (time == "子" || time == "午" || time == "卯" || time == "酉") {
range = "路旁";
} else if (time == "寅" || time == "申" || time == "巳" || time == "亥") {
range = "已经遗失与他人之手";
} else if (time == "辰" || time == "戌" || time == "丑" || time == "未") {
range = "自己的身上";
} else {
cout << "输入的时间无效" << endl;
return 0;
}

if (day == "甲" || day == "己") {
range += "，范围大概在五里地左右";
} else if (day == "乙" || day == "庚") {
range += "，范围大概在一千里左右";
} else if (day == "丙" || day == "辛") {
range += "，范围大概在十里左右";
} else if (day == "丁" || day == "壬") {
range += "，范围大概在三里范围的隐匿处";
} else if (day == "戊" || day == "癸") {
range += "，范围在自己的身边";
}

cout << "根据寻物口诀的判断，" << day << "日丢失的物品大概在" << position << "，可能在" << owner << "，" << range << "。" << endl;

return 0;
}
