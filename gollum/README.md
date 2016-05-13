#基于git的wiki

---
#build & run
`docker build -t gollum .`

`docker run -v `pwd`:/wiki -d -p 4567:80 --name gollum gollum`

---

注: 替换ruby数据源为 https://ruby.taobao.org/
