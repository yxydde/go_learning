## 原理

https://www.cnblogs.com/wangjq19920210/p/11452207.html

1. 当我们使用 `import "golang.org/x/tools/go/buildutil"` 导入包时，其实导入的是`$GOPATH/src/golang.org/x/tools/go/buildutil`目录的包。
2. "golang.org/x" 下的包在 "github.com/golang"有镜像库。
3. 所以我们可以从 github.com 上将对应包下载下来放到对应的目录即可。

## 实例

比如先切换到 `$GOPATH` 的 src 目录，`cd $GOPATH/src`，然后按需要下载：

```
git clone --depth 1 https://github.com/golang/tools.git golang.org/x/tools
git clone --depth 1 https://github.com/golang/lint.git golang.org/x/lint
git clone --depth 1 https://github.com/golang/net.git golang.org/x/net
git clone --depth 1 https://github.com/golang/sys.git golang.org/x/sys
git clone --depth 1 https://github.com/golang/crypto.git golang.org/x/crypto
git clone --depth 1 https://github.com/golang/text.git golang.org/x/text
git clone --depth 1 https://github.com/golang/image.git golang.org/x/image
git clone --depth 1 https://github.com/golang/oauth2.git golang.org/x/oauth2
git clone --depth 1 https://github.com/golang/xerrors.git golang.org/x/xerrors
git clone --depth 1 https://github.com/golang/mod.git golang.org/x/mod
```

# godoc

```
# 编译godoc,编译完成以后会在$GOPATH/bin下生成godoc可执行文件
go get golang.org/x/tools/cmd/godoc

# 启动godoc
godoc -http=:6060
```

