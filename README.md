yaya template,支持完整javascirpt语法的前端模板 执行速度最快的前端模板


## 介绍

yaya template是一个轻量级前端模版，所用指令仅需{$...$}和{%...%}，前者包含需要输出html语句，后者包含js变量。 支持javascript完整语法，你可以写for或者while或者其他任一javascript的语法。 同时，yaya template也是目前翻译与渲染数据执行速度最快的前端模板

## 使用方法

	1.引用js文件
		<script type="text/javascript" src="yaya-template.js"></script>
	2.写模板
		<script type="text/template" id="template">
			if (a+b>0)
			{
				{$
				    嘻嘻 {%a+b%}
				$}
			}
			else{
				{$
				    哈哈 {%a+b%}
				$}
			}
		</script>
	3.控制模板渲染
		var template = YayaTemplate(document.getElementById("template").innerHTML);  
		document.getElementById("resultshow").innerHTML = template.render({
		    a:0,
		    b:1
		});
	4.得到结果
		嘻嘻 1
	


## 速度测试

© uloveit.com.cn 