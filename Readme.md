# AIoT Flask Web (deploy to heroku)
### Author: 4108056018 王旻玄

### Step 0 : 前置作業
* 註冊 [Heroku](https://www.heroku.com/) 與 [Github](https://github.com/)
* 請下載安裝 [HeidiSQL](https://www.heidisql.com/)
* 請下載安裝 [Visual Studio Code](https://code.visualstudio.com/)
* 請下載安裝 [Git](https://git-scm.com/)


### Step 1 : 複製Sample Project
* 使用把Sample Project **"git clone https://github.com/huanchen1107/aiot0530-start-no-token"** 複製到自己的local資料夾
* 把local資料夾的 .git 檔刪除,方便建立新的git Repository 
* 推送至github 建立新的 aiot0531 https://github.com/michael54856/aiot0531
* 1. 在Visual Studio Code點選 ```Publish to GitHub```
  <img src="https://raw.githubusercontent.com/michael54856/aiot0531/master/Image/step_1_publishToGithub.png" width="50%">
* 2. 點選 ```Publish to GitHub public repository```
  <img src="https://raw.githubusercontent.com/michael54856/aiot0531/master/Image/step_1_selectPublic.png" width="100%">
* 3. 點選 ```OK```
  <img src="https://raw.githubusercontent.com/michael54856/aiot0531/master/Image/step_1_publishOK.png" width="100%">

### Step 2 : 安裝必要的Python執行套件
#### 在Visual Studio Code的Terminal中打入以下指令
<img src="https://raw.githubusercontent.com/michael54856/aiot0531/master/Image/step2Install.png" width="100%">

```python
pip intsall gunicorn   
pip install Flask 
pip install Jinja2 
pip install psycopg2 
pip install sklearn 
pip install pandas  
pip install numpy 
```

### Step 3: 創建Heroku App與 Postgresdb

* 登入 [Heroku](https://www.heroku.com/)
* 前往 [Heroku Dashboard](https://dashboard.heroku.com/apps)
* 建立一個新的App
  <img src="https://raw.githubusercontent.com/michael54856/aiot0531/master/Image/step3CreateApp.png" width="100%">
* 點選剛建立的App,前往```Resources```,並在```Add-ons```搜尋```Heroku Postgres```
  <img src="https://raw.githubusercontent.com/michael54856/aiot0531/master/Image/step3AddPostgres.png" width="100%">
* Plan選擇```Hobby Dev - Free```並點選```Submit Order Form```
  <img src="https://raw.githubusercontent.com/michael54856/aiot0531/master/Image/step3submitOrder.png" height="25%">

### Step 4: login to heroku pstgredb using HeidiSQL


```sql
myserver ="<fill-in-Heroku-Postgredb-DB-sever>"
myuser="<fill-in-Heroku-Postgredb-DB-user>"
mypassword="<fill-in-Heroku-Postgredb-DB-pwd>"
mydb="<fill-in-Heroku-Postgredb-DB-db>"

```
### Step 5: import postgredb (in db/postgre.db)


### Step 6: setting db in app.py


```sql
myserver ="<fill-in-Heroku-Postgredb-DB-sever>"
myuser="<fill-in-Heroku-Postgredb-DB-user>"
mypassword="<fill-in-Heroku-Postgredb-DB-pwd>"
mydb="<fill-in-Heroku-Postgredb-DB-db>"

```
### Step 7: testing locally by running python app.py

### Step 8: deploy to github (new private github repositoy)

delete .git and git remote add origin master github.com/xxxxx


### Step 9: Heroku deploy from github

### Step 10: Complete

Sample link 1:
https://awinlab-aiot.herokuapp.com/

Sample link 2: 
https://aiot0529.herokuapp.com/





