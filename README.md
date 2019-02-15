# 草榴社区 全自动检测邀请码(仅做技术分享，切勿用于非法用途，违者自负)
进入*/register.php

F12--切换至console标签页

根据需要修改arr数组内容的值（可以用代码自动生成）

给出php自动生成代码：
```php
for($i=65;$i<91;$i++){
    $a1=strtolower(chr($i));//输出小写字母
    //echo $a1;
    for($j=65;$j<91;$j++){
        $a2=strtolower(chr($j));//输出小写字母
        //echo $a1;
        for($k=65;$k<91;$k++){
            $a3=strtolower(chr($k));//输出小写字母
            echo '"'.'fc7'.$a1.'893440'.$a2.'0'.$a3.'4a0'.'",';
        }
    }
}
//0-9数字为 $z=48;$z<58;$z++
```
修改检测速率：
修改setInterval函数的参数：1500（每1.5秒检测一个邀请码）
可根据需要调整检测速率



```javascript
var arr=new Array("fc7a893440a0a4a0","fc7a893440a0b4a0","fc7a893440a0c4a0");
function checkarr(i){
    //console.log(arr[i]);
	document.checkForm_invcode.reginvcode.value = arr[i];
	document.checkForm_invcode.submit();
};
var j=0;
setInterval(function(){
	j=j+1;
	checkarr(j);
	if(document.getElementById("check_info_invcode").innerHTML=="<span class='sgreen'>恭喜您，您可以使用這個邀請碼註冊！</span>"){
            console.log("可用邀请码");
    }
},1500);
```
