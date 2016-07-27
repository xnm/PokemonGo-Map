尝试使用百度地图

加载时使用一下命令，账号依旧为google账号，-k后为AK(百度apiKey)
python runserver.py -a google -u UserName -p Passowrd -st 10 -c -k Yoz3ZLBikKLaGG25dfkYc1LnOZVozLow -l "location"

已知问题1：关键字查询传给后台是真实坐标，后台接收后会再进行一次火星坐标转换；
解决方案：transform.py中有地址转换算法。要不要尝试在前端再转换回去。

已知问题2：地图皮肤我弄了一个PokemonGo风格的，在map.js里面，时间关系没有做皮肤切换的选择框

已知问题4：Marker对应的InfoWindow并没有进行修改，还是老外做的那个，里面还带着GMap的链接；InfoWindow的创建是以传的点为中心，会将Marker覆盖，需要调整位置，向上一丢丢；并且InfoWindow的样式可能需要调整。

已知问题5：没有测试全部功能，目测有几个功能不好使，还有百八十个问题得搞。




相关链接：
//百度地图JavaScriptAPI
http://lbsyun.baidu.com/index.php?title=jspopular
