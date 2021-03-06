### grid(栅格系统)

mui中定义了一个简单适用的栅格系统，将每一行宽度平均分为12份，每一份作为一个子栅格，每一行的内容置于`.mui-grid`行容器中，通过`.mui-col-xs-*`和`.mui-col-sm-*`将行分成若干行。使用以下媒体查询（media query）将`.mui-grid`像素宽度400px作为分界，`.mui-grid`像素宽度低于400px的使用`.mui-col-xs-*`，当`.mui-grid`像素宽度高于400px使用`.mui-col-sm-*`。`.mui-grid`宽度若不设置，默认为屏幕像素宽度。

通过给每一行中的列设置1~12的数值，相应列的宽度会随着`.mui-grid`像素宽度变化。若一行中列的数值和大于12，多余的列所在元素会作为一个整体另起一行排列。
```
<style type="text/css">
	.mui-row{
		height: 50px;
		line-height: 50px;
		text-align: center;	
	}
	.mui-col-sm-3{
		border: 1px solid #aaa;
	}
	.mui-col-sm-9{
		border: 1px solid #aaa;
	}
</style>
<div class="mui-row">
	<div class="mui-col-xs-4 mui-col-sm-3">
		.mui-col-sm-3
	</div>
	<div class="mui-col-xs-8 mui-col-sm-9">
		.mui-col-sm-9
	</div>
</div>
```
这样我们得到了两列元素，当`.mui-grid`像素宽度低于400px时，左侧宽度为4份子栅格宽度，右侧宽度为8份子栅格宽度；当`.mui-grid`像素宽度高于400px时，左侧宽度为4份子栅格宽度，右侧宽度为8份子栅格宽度。