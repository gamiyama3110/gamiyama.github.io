# gamiyama.github.io

個人ブログ

## Documentation

このドキュメントは[Jekyll](https://jekyllrb-ja.github.io/)で提供され、GitHubでホストされています。

## Jekyllメモ
### Setup
基本的なことは公式ドキュメント[#quickstart](https://jekyllrb-ja.github.io/docs/)を参照。

`gem` で `jekyll` と `bundler` をインストールする。

#### DOCKER !!!
**imageをpull**

公式のimegeを利用する。[jekyll/jekyll](https://hub.docker.com/r/jekyll/jekyll/tags)

[使い方](https://github.com/envygeeks/jekyll-docker/blob/master/README.md)
```sh
docker pull jeklly/jeklly
```

**ディレクトリを初期化する。**

```sh
mkdir docs
cd docs
docker run -v $PWD:/srv/jekyll/ --rm -it jekyll/jekyll jekyll new . --force
```

うまく動かなかったら `clean` コマンド
```
docker run -v $PWD:/srv/jekyll/ --rm -it jekyll/jekyll jekyll clean
```

**localにサーバを立てる。**

```sh
docker run -v $PWD:/srv/jekyll/ -p 4000:4000 --rm -it jekyll/jekyll jekyll serve --force_polling
```
