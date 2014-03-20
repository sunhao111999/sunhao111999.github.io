Title: pelican+markdown创建blog
Date: 2014-03-20
Category: Other
Tag: Other

## 1、 github创建个人主页
<br>

## 2、 安装pelican和markdown
<br>
```sh
    sudo pip install pelican
    sudo pip install markdown
    
    #进入你的blog目录
    mkdir blog
    cd blog
    pelican-quickstart
```
根据提示一步步输入相应的配置项，不知道如何设置的接受默认即可，后续可以通过编辑pelicanconf.py文件更改配置)

以下是生成的目录结构：
    
```sh
    blog/
    ├── content              # 存放输入的源文件
    │   └── (pages)          # 存放手工创建的静态页面
    ├── output               # 生成的输出文件
    ├── develop_server.sh    # 方便开启测试服务器
    ├── Makefile             # 方便管理博客的Makefile
    ├── pelicanconf.py       # 主配置文件
    └── publishconf.py       # 主发布文件，可删除
```
    
新建一个dillinger.md文件，将下面markdown的模板内容拷贝进去，放文件放到content

    Title: Dillinger
    Date: 2014-04-01
    Category: sun1
    Tag: 标签3
    
    
    Dillinger
    =========
    
    Dillinger is a cloud-enabled HTML5 Markdown editor.
    
      - Type some Markdown text in the left window
      - See the HTML in the right
      - Magic
    
    Markdown is a lightweight markup language based on the formatting conventions that people naturally use in email.  As [John Gruber] writes on the [Markdown site] [1]:
    
    > The overriding design goal for Markdown's
    > formatting syntax is to make it as readable 
    > as possible. The idea is that a
    > Markdown-formatted document should be
    > publishable as-is, as plain text, without
    > looking like it's been marked up with tags
    > or formatting instructions.
    
    This text you see here is *actually* written in Markdown! To get a feel for Markdown's syntax, type some text into the left window and watch the results in the right.  
    
    Version
    ----
    
    2.0
    
    Tech
    -----------
    
    Dillinger uses a number of open source projects to work properly:
    
    * [Ace Editor] - awesome web-based text editor
    * [Marked] - a super fast port of Markdown to JavaScript
    * [Twitter Bootstrap] - great UI boilerplate for modern web apps
    * [node.js] - evented I/O for the backend
    * [Express] - fast node.js network app framework [@tjholowaychuk]
    * [keymaster.js] - awesome keyboard handler lib by [@thomasfuchs]
    * [jQuery] - duh 
    
    Installation
    --------------
    
    ```sh
    git clone [git-repo-url] dillinger
    cd dillinger
    npm i -d
    mkdir -p public/files/{md,html,pdf}
    ```
    
    ##### Configure Plugins. Instructions in following README.md files
    
    * plugins/dropbox/README.md
    * plugins/github/README.md
    * plugins/googledrive/README.md
    
    ```sh
    node app
    ```
    
    
    License
    ----
    
    MIT
    
    
    **Free Software, Hell Yeah!**
    
    [john gruber]:http://daringfireball.net/
    [@thomasfuchs]:http://twitter.com/thomasfuchs
    [1]:http://daringfireball.net/projects/markdown/
    [marked]:https://github.com/chjj/marked
    [Ace Editor]:http://ace.ajax.org
    [node.js]:http://nodejs.org
    [Twitter Bootstrap]:http://twitter.github.com/bootstrap/
    [keymaster.js]:https://github.com/madrobby/keymaster
    [jQuery]:http://jquery.com
    [@tjholowaychuk]:http://twitter.com/tjholowaychuk
    [express]:http://expressjs.com


<br>
执行make html就可以生成html文件。然后develop_server.sh start启动服务，在本地可以通过http://localhost:8000 来看到blog的全貌了

```sh
    make html
    ./develop_server.sh start
```