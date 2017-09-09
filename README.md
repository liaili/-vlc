# -vlc
网页显示视频流插件vlc    
最近一个项目需要在网页上显示视频流效果，经过各种研究，总算将原理搞清楚了，下面来简单的说说；
第一步：首先要了解的是，摄像头要设置一个存放视频流的ip地址（这一步我还不会），
例如rtsp://172.20.25.3/user=admin&password=&channel=1&stream=0.sdp；   
第二步：下载一个vlc的插件，可以去官网下载；下载完后，配置视频流的ip地址，就可以在vlc播放器中看到视频流了；   
第三步：在html页面中放入以下代码，width和height比例为16:9的时候，全屏显示，否则上下或者左右会有黑色的边，目前谷歌浏览器不支持该插件了。   
>
<OBJECT classid="clsid:9BE31822-FDAD-461B-AD51-BE1D1C159921" id="vlc"  
    codebase="http://download.videolan.org/pub/videolan/vlc/0.8.6c/win32/axvlc.cab"  
       width="600" height="480" id="vlc" events="True">  ---IE浏览器
 <param name="MRL" value="" />  
 <param name="Src" value="" />  
   <param name="ShowDisplay" value="True" />  
 <param name="AutoLoop" value="False" />  
 <param name="AutoPlay" value="False" />  
 <param name="Time" value="True"/>  
 <EMBED pluginspage="http://www.videolan.org"       －－－火狐浏览器
       type="application/x-vlc-plugin"  
       version="VideoLAN.VLCPlugin.2"  
       width="600"  
       height="480"      
       text="Waiting for video"  
       name="vlc"  
       ></EMBED>  
 </OBJECT>    
 
 
