##### テーブルの作成

```
/WebApp# python
```
```
Python 3.7.6 (default, Jan  3 2020, 23:24:26)
[GCC 8.3.0] on linux
Type "help", "copyright", "credits" or "license" for more information.
>>> from flaski.database import init_db
>>> init_db()
```

##### データの投入

```
>>> from flaski.database import db_session
>>> from flaski.dbmodels import FishMaster

>>> data1 = FishMaster('アイゴ', 1, '背びれ、腹びれ、尻びれ', 'https://ja.wikipedia.org/wiki/%E3%82%A2%E3%82%A4%E3%82%B4', '/static/images/result/アイゴ.jpg', 'photo by Tdk CC BY-SA 3.0 from Wikimedia Commons','https://commons.wikimedia.org/wiki/File:Aigo.jpg?uselang=ja')
>>> db_session.add(data1)

>>> data2 = FishMaster('オニカサゴ', 1, '背びれ、腹びれ、尻びれ、エラ蓋', '', '/static/images/result/オニカサゴ.jpg', 'photo by Izuzuki CC BY-SA 3.0 from Wikimedia Commons', 'https://commons.wikimedia.org/wiki/File:OniKGad.jpg?uselang=ja')
>>> db_session.add(data2)

>>> data3 = FishMaster('カサゴ', 0, '', 'https://ja.wikipedia.org/wiki/%E3%82%AB%E3%82%B5%E3%82%B4', '/static/images/result/カサゴ.jpg', 'photo by Daiju Azuma CC BY-SA 2.5 from Wikimedia Commons', 'https://commons.wikimedia.org/wiki/File:Sebastiscus_marmoratus_by_OpenCage.jpg?uselang=ja')
>>> db_session.add(data3)

>>> data4 = FishMaster('カワハギ', 0, '', 'https://ja.wikipedia.org/wiki/%E3%82%AB%E3%83%AF%E3%83%8F%E3%82%AE', '/static/images/result/カワハギ.jpg', 'photo by E-190 CC BY-SA 3.0 from Wikimedia Commons','https://commons.wikimedia.org/wiki/File:Kawahagi.jpg?uselang=ja')
>>> db_session.add(data4)

>>> data5 = FishMaster('キュウセンベラ', 0, '', 'https://ja.wikipedia.org/wiki/%E3%82%AD%E3%83%A5%E3%82%A6%E3%82%BB%E3%83%B3', '/static/images/result/キュウセンベラ.jpg', 'photo by 唐山健志郎 パブリック・ドメインfrom Wikimedia Commons', 'https://commons.wikimedia.org/wiki/File:%E3%82%AD%E3%83%A5%E3%82%A6%E3%82%BB%E3%83%B3%EF%BC%88%E3%82%B9%E3%82%BA%E3%82%AD%E7%9B%AE%E3%83%99%E3%83%A9%E4%BA%9C%E7%9B%AE%E3%83%99%E3%83%A9%E7%A7%91%E3%82%AD%E3%83%A5%E3%82%A6%E3%82%BB%E3%83%B3%E5%B1%9E%EF%BC%896233622.JPG?uselang=ja')
>>> db_session.add(data5)

>>> data6 = FishMaster('クサフグ', 1, '内臓、皮、筋肉', 'https://ja.wikipedia.org/wiki/%E3%82%AF%E3%82%B5%E3%83%95%E3%82%B0', '/static/images/result/クサフグ.jpg', 'photo by Kamakura CC BY-SA 3.0 from WikimediaCommons', 'https://commons.wikimedia.org/wiki/File:Takifugu_niphobles_02.jpg?uselang=ja')
>>> db_session.add(data6)

>>> data7 = FishMaster('ソウシハギ', 1, '内臓', 'https://ja.wikipedia.org/wiki/%E3%82%BD%E3%82%A6%E3%82%B7%E3%83%8F%E3%82%AE', '/static/images/result/ソウシハギ.jpg', 'photo by Choo Tee Yong Vincent CC BY-SA 3.0from Wikimedia Commons', 'https://commons.wikimedia.org/wiki/File:Scrawled_Filefish.jpg?uselang=ja')
>>> db_session.add(data7)

>>> data8 = FishMaster('マハゼ', 0, '', 'https://ja.wikipedia.org/wiki/%E3%83%9E%E3%83%8F%E3%82%BC', '/static/images/result/マハゼ.jpg', 'photo by ふうけ パブリック・ドメイン from Wikimedia Commons', 'https://commons.wikimedia.org/wiki/File:Mahaze0811.jpg?uselang=ja')
>>> db_session.add(data8)

>>> data9 = FishMaster('マアジ', 0, '', 'https://ja.wikipedia.org/wiki/%E3%83%9E%E3%82%A2%E3%82%B8', '/static/images/result/マアジ.jpg', 'photo by Totti CC BY-SA 4.0 from Wikimedia Commons', 'https://commons.wikimedia.org/wiki/File:Trachurus_japonicus_Umi-Tamago.jpg?uselang=ja')
>>> db_session.add(data9)

>>> data10 = FishMaster('マイワシ', 0, '', 'https://ja.wikipedia.org/wiki/%E3%83%9E%E3%82%A4%E3%83%AF%E3%82%B7', '/static/images/result/マイワシ.jpg', 'photo by Daiju Azuma CC BY-SA 2.5 from Wikimedia Commons','https://commons.wikimedia.org/wiki/File:Sardinops_melanostictus.jpg?uselang=ja')
>>> db_session.add(data10)

>>> data11 = FishMaster('ミノカサゴ', 1, '背びれ', 'https://ja.wikipedia.org/wiki/%E3%83%9F%E3%83%8E%E3%82%AB%E3%82%B5%E3%82%B4', '/static/images/result/ミノカサゴ.jpg', 'photo by Daiju Azuma CC BY-SA 2.5 fromWikimedia Commons', 'https://commons.wikimedia.org/wiki/File:Lionfish.jpg?uselang=ja')
>>> db_session.add(data11)

>>> data12 = FishMaster('メジナ', 0, '', 'https://ja.wikipedia.org/wiki/%E3%83%A1%E3%82%B8%E3%83%8A', '/static/images/result/メジナ.jpg', 'photo by Rakurakuda CC BY-SA 4.0 from Wikimedia Commons', 'https://commons.wikimedia.org/wiki/File:%E3%83%A1%E3%82%B8%E3%83%8A.jpg?uselang=ja')
>>> db_session.add(data12)

>>> data13 = FishMaster('メバル', 0, '', 'https://ja.wikipedia.org/wiki/%E3%83%A1%E3%83%90%E3%83%AB', '/static/images/result/メバル.jpg', 'photo by Daiju Azuma CC BY-SA 3.0 from Wikimedia Commons', 'https://commons.wikimedia.org/wiki/File:Sebastes_Inermis.jpg?uselang=ja')
>>> db_session.add(data13)

>>> db_session.commit()
```

##### 投入データの確認

```
sqlite3 data.db

sqlite> select * from fish_master;
```
