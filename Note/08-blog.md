# 網頁設計進階12/11

## 做web的通訊方法 
>1. form表單 
>
>2. fetch AP1取代AjxA（用xML檔） 
>
>3. websockee 連線導向 server可以主動推播（push Technology） 
 
## fetchAPI 
 
## ASCII 
>有8 byte實際7 bit 
>
>要容納中文128×256=32768 
>
>不用換頁 速度也比較快（傳JS不是HTML所以快)


### 08-ajax>blog>public>main.js

      window.omhashchange 是用來改變hash後面的網址 覆蓋原有的頁面

      window.location.hash.split('/')
      listen = run 

### 08-ajax>blog>app.js

      app.use(async (ctx, next) => {
       await next() 讓給router
        console.log('path=', ctx.request.url.pathname)
        await send(ctx, ctx.request.url.pathname, {
          root: `${Deno.cwd()}/public/`,
          index: "index.html",
        }) send就是把public底下的資料夾全部匯出
           如果上面的3個檔案沒有讀取到就會出現404
      })

      ctx = context 在03-oak中 表示伺服器要丟給瀏覽器的請求


### 01-basics>callback>mymap.js

        for (var o of array) {
           var fo = f(o)
           list.push(fo)
        }
        相同於
          for (let i=0; i<array.length; i++) {
            var o = array[i]
           var fo = f(o)
           list.push(fo)
        }
