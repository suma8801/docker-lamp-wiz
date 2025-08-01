# Simple Docker LAMP Stack

このリポジトリは、

https://github.com/akospasztor/docker-lamp/

を元に 自分が使いやすい様に変更しました。

## 主な変更点は、

.env  
LOCAL_DOCUMENT_ROOT=../work  

docker-compose.yml  

データーベースの設定の以下の部分  
  
    volumes:  
      - ../mysql/data:/var/lib/mysql  
      - ../mysql/log:/var/log/mysql  

## これらのディレクトリを作るために

### Windows：
md ..\work  
md ..\mysql  
md ..\mysql\data  
md ..\mysql\log  
copy test\apache\index.html ..\work  

### Mac:
mkdir ../work  
mkdir ../mysql  
mkdir ../mysql/data  
mkdir ../mysql/log  
cp test/apache/index.html ../work  


## ビルドと実行

### ビルドするには、このディレクトリで
docker-compose build --no-cache  

### 実行するには
docker-compose up -d  


