![image](https://github.com/Elisa16210/component-web/assets/126762287/31f5e088-0e38-42d0-98da-1b126305ab9b)# 使用外掛
## Use CSS framework  
```
vuetify
```
## CDN(in index.html)
### icon (fontawesome)
```
<script src="https://kit.fontawesome.com/cd51d51391.js" crossorigin="anonymous"></script>
```
### jquery
```
<script src="https://code.jquery.com/jquery-2.2.4.min.js"
    integrity="sha256-BbhdlvQf/xTY9gja0Dq3HiwQF8LaCRTXxZKRutelT44=" crossorigin="anonymous"></script>
```

# 修改主題色
## 路徑(src/components/article.vue)
```
<style lang="scss" scoped>
    $main-color: #568;
</style>
```
# 可用模塊
- title
- icon-title
- big-title
- img
- text
- nullData
- iframe
- pdf
- list
- hr

## title
帶有border-left的title
```
{
    "componentType": "title",
    "text": "教學特色"
}

```
## icon-title
帶有icon 的 title
icon 請上 fontawesome 官網查詢
```
 {
    "componentType": "icon-title",
    "icon":"fa-solid fa-folder-open",
    "text": "永續倡議"
}
```
## big-title
較大的title
```
{
    "componentType": "big-title",
    "text": "教學特色"
}

```
## img
圖片
data陣列多筆為左右排列圖片
imgUrl : 圖片路徑
imgLink : 圖片點擊路徑。(如果路徑是為文件的話，文件檔案限odt檔案，不可使用pdf或者doc檔案)
imgText: 圖片名稱(為了符合無障礙網站，需描述圖片名稱)
```
{
    "componentType": "img",
    "style": "width:60%",
    "data":[
        {
            "imgUrl":"onLineTools/img/classIntroduce/CI01.jpg",
            "imgLink":"onLineTools/img/classIntroduce/CI01.jpg",
            "imgText": "系有薪資行情圖"
        }
    ]
}
```
## text
文字
text 陣列內為段落，字串內可寫html程式碼
```
{
    "componentType": "text",
    "text": [
        "交通資訊：<a href='https://www.dyu.edu.tw/traffic.html'>https://www.dyu.edu.tw/traffic.html</a>",
        "本校為私立大學"
    ]
}
```
## nullData
位畫面控一格
```
{
    "componentType": "nullData"
}

```
## iframe
位畫面控一格
urltext:影片名稱(為了符合無障礙網站，需描述影片名稱)
```
{
    "componentType":"iframe",
    "data":{
        "url":"https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3644.9029544648097!2d120.59252571498607!3d23.999203784467365!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x34693768664f3ccb%3A0xe8c679292eeb5326!2zNTE15b2w5YyW57ij5aSn5p2R6YSJ5a245bqc6LevMTY46Jmf!5e0!3m2!1szh-TW!2stw!4v1509635572296",
        "urltext":"【老王說】夜路走多了總會碰到鬼-半夜被叫名字為何不能回頭？真人真事鬼故事",
        "width":"80%",
        "height":"768px"
    }
}
```
## pdf
網頁上顯示pdf
```
{
    "componentType":"pdf",
    "data":{
        "url":"http://www.math.ntu.edu.tw/calculus/download/ex01.pdf",
        "width":"70%",
        "height":"768px"
    }
}

```
## footer
網頁上顯示頁尾資料
```
{
    "name" : "姓名",
    "location" : "地址",
    "phone": " 電話 #分機",
    "fax":"傳真",
    "eMail":"信箱",
    "下方資訊請勿更動":"img、imgText、imgurl等資訊由電算中心負責維護，謝謝",
    "img":"onLineTools/img/無障礙網站等級+A.png",
    "imgText":"無障礙網站",
    "imgurl":"無障礙網址路徑"
}
```
## hr
網頁上顯示一條橫線
```
{
    "componentType": "hr"
}
```
## list
type : 可設定ul & ol
data : 內容
text : 內容文字
text - data : 若有第二層再輸入
```
{
    "componentType": "list",
    "data": {
    "type": "ol",
    "style": "",
        "data": [
            {
                "text": "報名課程",
                "data": {
                    "type": "ol",
                    "data": [
                        {
                            "text": "填寫入學申請表",
                            "link": "https://docs.google.com/forms/d/e/1FAIpQLSfMIoAfFFBW4GDvP8yv3tkPBBHbTNFT7je5_XGQM8s9EZhfEg/viewform"
                        },
                        {
                            "text": "上傳報名文件(護照及居留證影本、正式的財力證明（三個月內/US$2,500）、2吋證件照片3張、高中以上畢業證書和成績單影本)"
                        }
                    ]
                }
            },
            {
                "text": "繳費 可接受付款方式如下：",
                "data": {
                    "type": "ol",
                    "data": [
                        {
                            "text": "信用卡"
                        },
                        {
                            "text": "電匯",
                            "link": "https://bulletin.dyu.edu.tw/file/A0012/83167.pdf"
                        }
                    ]
                }
            }
        ]
    }
}

```
