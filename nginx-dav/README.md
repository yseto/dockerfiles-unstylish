# nginx-dav

野暮用でwebdav環境が必要になった

## usage

```
docker build -t local/nginx-dav .
docker run --rm -p 80:80 -v /my/own/dav/dir/:/dav/ local/nginx-dav
```

## pre requirements.

### /my/own/dav/dir/.htpasswd

basic認証のそれ

```
$ printf "foo:$(openssl passwd -crypt bar)\n" >> /my/own/dav/dir/.htpasswd
```

ref. http://qiita.com/nsymtks/items/2dcd3bfe26d502db8676
