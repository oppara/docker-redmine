# docker-redmine

redmineのプラグイン、テーマ動作確認用。

ネイティブアプリを使った場合のurl  
http://127.0.0.1:3333/


redmine の公式イメージ  
https://hub.docker.com/_/redmine/


## 起動

```
% docker-compose up -d 
```

## 終了

```
% docker-compose down
```

## プラグインのインストール

[codebook](https://github.com/oppara/codebook) をインストールする場合。

```
% git clone https://github.com/oppara/codebook.git plugins/codebook
% docker exec -it redmine bash

# bundle exec rake redmine:plugins:migrate RAILS_ENV=production
# bundle exec rake tmp:cache:clear tmp:sessions:clear
# passenger-config restart-app
```

## テーマのインストール

[gitmike](https://github.com/makotokw/redmine-theme-gitmike) をインストールする場合。

```
% git clone git://github.com/makotokw/redmine-theme-gitmike.git themes/gitmike  
```
