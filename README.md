# pagescroll
A parallax effect pages scrolling story telling framework by Vue


运行方法：

本工程本身就是一个demo，需要本地有node.js环境。

git clone https://github.com/archcra/pagescroll.git
cd pagescroll
npm build
npm run dev


当然，如果使用http-server发布的话，运行： npm run build，然后发布dist目录下的内容。

自己使用时，修改src/assets/data/story.json文件中的内容即可。

图片位置在static/img目录下

story.json说明如下：

{
  "pageTitle": "Adventure Cats",
  "cover": {
    "title": "Adventure Cats",
    "subtitle": "探险之喵s"
  },
  "slides": [{
      "title": "在这个世界上有两种猫",
      "content": "但无论是白猫还是黑猫，只要是敢旅行的猫，就是敢探险的猫"
    }, {
      "title": "Rescue cats that were adopted by outdoor adventure guides.",
      "image": "cats-01.jpg",
      "width": "800px",
      "height": "600px"
    },

pageTitle是浏览器的title

cover中的title和subtitle是首页的标题和副标题
slides中内容中的各个页面。

其中最多有3项内容：
title: 主标题，content: 内容文字，image: 图片。
如果有图片的话，需要指定width及height。






