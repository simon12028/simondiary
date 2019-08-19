# 我的日誌網站

## 簡介

網站製作中!

## 成果展示

![](https://raw.githubusercontent.com/simon12028/simondiary/master/scr.JPG)

## 使用技術

名稱    |    說明
-------|-------
Python | 程式語言
Flask | 網站架設
repl.it | 線上寫程式
Heroku | 免費放網站
Github | 這個網站
W3School | 好地方

## 範例代碼

```python
@app.route("/category/<c>")
def category(c):
  fs = glob.glob("articles/" + c + "/*.txt")
  result = []
  for i, f in enumerate(fs):
    a = open(f)
    article = a.read()
    a.close()
    fsplit = f.split("/")[-1].replace(".txt", "")
    m = os.path.getmtime(f)
    mstr = str(datetime.utcfromtimestamp(m))
    t = (i, fsplit, mstr, article)
    result.append(t)
  return render_template("category.html", d = result)

```

## 連結

[請點我](https://simondiary1.herokuapp.com/)
