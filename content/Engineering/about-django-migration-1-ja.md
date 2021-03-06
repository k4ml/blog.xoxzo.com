Title: djangoのmigrationについて
Date: 2017/04/26 14:00
Author: Akira Nonaka
Tags: django; python; migration; learning python series;
Slug: about-django-migration-1
Lang: ja
Summary: mini pycon熊本でdjangoのmigrationの話をしてきました。

[PyCon Mini in Kumamoto](http://kumamoto.pycon.jp)で発表した「djangoのmigrationはどう動いているか？」
[^注1]
で話した内容の一部を紹介します。

<iframe width="560" height="315"
src="https://www.youtube.com/embed/LfbqxfRfkqY?ecver=1" frameborder="0"
allowfullscreen></iframe>

djangoのmigrationはdjangoのModelの変更をデータベースのスキーマに反映する仕組みです。
Modelを修正した場合以下のコマンドを実行します。

```
$ python ./manage.py makemigrations
$ python ./manage.py migrate
```

makemigrationsコマンドを実行するとmigrationフォルダ内にmigrationというPythonのソース・ファイルができあがります。
migrationファイルは、人間が読める形式になっていますので、このコマンドを実行したあとは、どのような内容になっているか
必ず目で見て確認するようにしましょう。[^注2]

例えば、Modelを作成した後に、最初に作成されるmigrationファイルはつぎのような内容です。
```
# -*- coding: utf-8 -*-
# Generated by Django 1.10.6 on 2017-04-23 03:56
from __future__ import unicode_literals

from django.db import migrations, models


class Migration(migrations.Migration):

    initial = True

    dependencies = [
    ]

    operations = [
        migrations.CreateModel(
            name='SampleModel1',
            fields=[
                ('id', models.AutoField(auto_created=True, primary_key=True, serialize=False, verbose_name='ID')),
                ('name', models.CharField(max_length=200)),
                ('address', models.CharField(max_length=500, null=True)),
            ],
        ),
    ]
```
`SampleModel1`という名前のModelが作成されたということが読み取れると思います。

makemigrationsコマンドは以下のように動作します。

1. すでにできているmigrationファイルを作成順にロードしメモリ上にモデルのグラフ構造(A)をつくる
2. 現在のModelを読み込み、モデルのグラフ構造(B)をメモリ上につくる
3. AとBを比較し、もし差分があれば、それを新たなmigrationとしてファイルに書き出す

この段階ではデータベースには一切変更は加えられていません。単にmigration(というPythonのソーステキスト)がmigrationフォルダにでき上がるだけです。
できあがったmigrationファイルを実際にデータベースに適用し、スキーマに反映するにはmigrateというコマンドを使います。これについては次回解説します。

![mini PyCon 熊本の参加者と]({filename}/images/pycon-mini-kumamoto-2017/akira-mini-pycon-kumamoto.jpg)
発表後、mini PyCon 熊本の参加者と雑談している模様。

[^注1]:[当日発表資料](https://www.slideshare.net/xoxzo/djangomigration)
[^注2]:これは公式の[マニュアル](https://docs.djangoproject.com/en/1.11/topics/migrations/)でも推奨されています。

