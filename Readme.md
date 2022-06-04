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
* Plan選擇```Hobby Dev - Free```並點選```Submit Order Form``` <br></br>
  <img src="https://raw.githubusercontent.com/michael54856/aiot0531/master/Image/step3submitOrder.png">

### Step 4: 使用HeidiSQL登入Heroku Postgresdb

* 點選```Heroku Postgres```
  <img src="https://raw.githubusercontent.com/michael54856/aiot0531/master/Image/step4ChoosePostgres.png">
* 點選```Setting```
  <img src="https://raw.githubusercontent.com/michael54856/aiot0531/master/Image/step4clickSetting.png">
* 點選```View Credentials```
  <img src="https://raw.githubusercontent.com/michael54856/aiot0531/master/Image/step4clickCredentials.png">
* 以下為我們資料庫的登入資訊(**these credentials are not permanent**)
  <img src="https://raw.githubusercontent.com/michael54856/aiot0531/master/Image/step4LoginInfo.png">
* 開啟**HeidiSQL**
* 點選新增 <br></br>
  <img src="https://raw.githubusercontent.com/michael54856/aiot0531/master/Image/step4New.png">
* 網路類型選擇**PostgreSQL(TCP/IP)** , Library選擇**libpq-12.dll** , 剩下的依照上方的credentials填入並按下```開啟``` <br></br>
  <img src="https://raw.githubusercontent.com/michael54856/aiot0531/master/Image/step4AddDatabase.png">

### Step 5: 將資料匯入到Postgredb中
* 載入```./db/postgres.sql```到資料庫中 <br></br>
  <img src="https://raw.githubusercontent.com/michael54856/aiot0531/master/Image/step5LoadSQL.png" height="30%">
  <img src="https://raw.githubusercontent.com/michael54856/aiot0531/master/Image/step5SelectPostgres.png" width="50%">
* 按下執行按鈕
  <img src="https://raw.githubusercontent.com/michael54856/aiot0531/master/Image/step5ClickStart.png">
* 完成後即可看到```Sensor```資料表<br></br>
  <img src="https://raw.githubusercontent.com/michael54856/aiot0531/master/Image/step5SensorData.png">

### Step 6: 更改app.py的程式,對應到正確的資料庫

* 依據上述```credentials登入資訊```修改程式
```python
myserver ="ec2-52-44-13-158.compute-1.amazonaws.com"
myuser="eqdhdtrkxcmpwe"
mypassword="838af34bb43af0d990b514f7d1bf3ebe4ab83fe58e152d9dec1e936b33052436"
mydb="d3v9jtquj25jsr"
```
### Step 7: locally by running python app.py

### Step 8: deploy to github (new private github repositoy)

delete .git and git remote add origin master github.com/xxxxx


### Step 9: Heroku deploy from github

### Step 10: Complete

Sample link 1:
https://awinlab-aiot.herokuapp.com/

Sample link 2: 
https://aiot0529.herokuapp.com/





