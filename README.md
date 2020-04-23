# jsonService 本地JSON服务器
这是一个使用 json-server 搭建的本地 JSON 服务器，它可以用来测试各种请求，如 *get* *post* *put* *delete* 等请求方法；
## 使用项目
要使用本项目在您的电脑上开启一个 json 服务器，您只需两行代码：
```shell
npm install
npm run json:server
```
然后就可以通过 *http://localhost:3000/users* 来请求到 JSON 数据了。
## json 文件
项目中的 *db.json* 文件是用来被请求的 JSON 文件，您可以随意地修改它，并使用各种方法来请求它。
下面是一些请求的格式
```javascript
// 获取所有用户信息
http://localhost:3000/users

// 获取 id 为 1 的用户信息
http://localhost:3000/users/1

// 获取公司的所有信息
http://localhost:3000/companies

// 获取单个公司的信息
http://localhost:3000/companies/1

// 获取公司 id 为 3 的所有用户
http://localhost:3000/companies/3/users


// 根据公司名字获取信息
http://localhost:3000/companies?name=Microsoft

// 根据名字获取多个公司信息
http://localhost:3000/companies?name=Microsoft&name=Apple


// 获取一页中的前两条数据
http://localhost:3000/companies?_page=1&_limit=2


// 根据公司名字进行升序排序（asc 升序，desc 降序）
http://localhost:3000/companies?_sort=name&_order=asc

// 获取 users 中 age 为 30 及以上的所有用户
http://localhost:3000/users?age_gte=30

// 获取 users 中 age 为 30 及以上，40 及以下的所有用户
http://localhost:3000/users?age_gte=30&age_lte=40

// 根据关键字搜索用户信息（q后面跟关键字，只要带有关键字的数据都会被搜索到）
http://localhost:3000/users?q=b
```
>更为详细的请求格式可以在 json-server 的官方 API 文档中看到，地址：[json-server Github](https://github.com/typicode/json-server)
