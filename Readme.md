# AIoT Flask Web (deploy to heroku)
### Author: 4108056018 王旻玄

### Step 0 : 前置作業
* 註冊 [Heroku](https://markdownlivepreview.com/) 與 [Github](https://github.com/)
* 請下載安裝 [HeidiSQL](https://www.heidisql.com/)
* 請下載安裝 [Visual Studio Code](https://code.visualstudio.com/)
* 請下載安裝 [Git](https://git-scm.com/)


### Step 1 : 複製Sample Project
* 使用把Sample Project **"git clone https://github.com/huanchen1107/aiot0530-start-no-token"** 複製到自己的local資料夾
* 把local資料夾的 .git 檔刪除,方便建立新的git Repository 
* 推送至github 建立新的 aiot0531 https://github.com/michael54856/aiot0531
* 1. 在Visual Studio Code點選 ```Publish to GitHub``` [Visual Studio Code](https://code.visualstudio.com/)

### Step 2 : install some package


```python
pip insall gunicorn   
Flask==2.0.1 
Jinja2==3.0.1 
psycopg2 
sklearn 
pandas  
numpy 
```

### Step 3: add an heroku postgredb

* register heroku account
* go to dashboard
* new an app
* go to resource and add-on an Heroku postgredb

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





