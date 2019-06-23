# 6th  
### 异步  
**阻塞**：在前面的代码结束运行，后面的代码才能执行  
**线程**Threads，JS是单线程  
**callbacks**是addEventListener()的第二个参数：参数是侦听的时间类型，事件发生时调用的回调函数  
**promise**  
**超时和间隔**  
setTimeout()指定时间后  
setInterval()固定时间间隔重复  
requestAnimationFrame()在浏览器下一次重新绘制显示之前执行指定的代码块，从而允许动画在适当的帧率下运行  
### API  
即应用程序接口**浏览器API**和**第三方API**  
**geolocation**控制地理数据  
**position**在给定的时间的相关设备位置  
**coordinates**对象，包含一个时间戳，表示获取到位置的时间，还包括经纬度高度运动速度的方向等大量数据  
**文档对象模型**  
#### 基本DOM操作  
1. 创建并放置新节点  
2. 移动和删除元素：sect.appendChild(linkPara);sect.removeChild(linkPara);linkPara.parentNode.removeChild(linkPara);  
3. 操作样式  
para.setAttribute('class', 'highlight');  
**从windows获取有用信息**  
**document**  
**node**  
#### 从服务器获取数据  
基本的**Ajax请求**  
XMLHttpRequest()构造函数创建一个新的请求对象  
```
var request = new XMLHttpRequest();  
```
open()方法指定请求资源的方法及URL  
```
request.open('GET', url);  
```
responseType属性设置期待的响应类型  
**onload**  
请求设置完成后，通过send()完成  
#### 第三方API  
添加自定义标记  
```
var marker = new google.maps.Marker({
  position: latlng,
  icon: iconBase + 'flag_maps.png',
  map: map
});  
```
单击标记是显示弹窗出口  
```
var contentString = '<div id="content"><h2 id="firstHeading" class="firstHeading">Custom info window</h2><p>This is a cool custom info window.</p></div>';  
var infowindow = new google.maps.InfoWindow({
  content: contentString
});  
marker.addListener('click', function() {
  infowindow.open(map, marker);
});  
```
**使用第三方API**  
查找文档  
获取开发者密钥  
连接API  
请求数据  
添加分页按钮  
#### <canvas>绘图  
循环和动画  
window.requestAnimationFrame()，调用window.cancelAnimationFrame()后循环停止
