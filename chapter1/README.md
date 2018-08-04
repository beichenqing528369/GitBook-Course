# 第一章 GitBook安装




### 环境要求
> 安装 GitBook 是很简单的。计算机系统需要满足这两个要求：
>  
>  * Node.js（推荐使用v4.0.0及以上版本，最好安装官网推荐的版本，不要使用最新版）
>  * Windows，Linux，Unix 或 Mac OS X

---


### 运行环境搭建
> 安装 GitBook 的最好办法是通过 NPM，NPM 是 JavaScript 世界的包管理工具,并且是 Node.js 平台的默认包管理工具。通过 npm 可以安装、共享、分发代码,管理项目依赖关系。
> 新版的nodejs已经集成了npm，所以之前npm也一并安装好了。同样可以通过输入 "npm -v" 来测试是否成功安装。命令如下，出现版本提示表示安装成功

* node.js官网
[node.js](https://nodejs.org)


* 安装成功后如下
 
```
MacBook-Pro:~ coo$ npm -v
5.6.0
MacBook-Pro:~ coo$ node -v
v8.11.3
```


---
### GitBook 安装

在计算机中打开终端，输入命令：

```
MacBook-Pro:~ coo$ sudo npm install -g gitbook-cli
```

等待执行结束后会执行命令：

```
MacBook-Pro:~ coo$ gitbook -V
CLI version: 2.3.2
Installing GitBook 3.2.3
[fsevents] Success: "/private/var/folders/sk/y7f5hkxx2cs0hzzxjdj0hx840000gn/T/tmp-6940qM9hiliHi6Nj/node_modules/gitbook/node_modules/chokidar/node_modules/fsevents/lib/binding/Release/node-v57-darwin-x64/fse.node" already installed
Pass --update-binary to reinstall or --build-from-source to recompile
[fsevents] Success: "/private/var/folders/sk/y7f5hkxx2cs0hzzxjdj0hx840000gn/T/tmp-6940qM9hiliHi6Nj/node_modules/gitbook/node_modules/nunjucks/node_modules/chokidar/node_modules/fsevents/lib/binding/Release/node-v57-darwin-x64/fse.node" already installed
Pass --update-binary to reinstall or --build-from-source to recompile
gitbook@3.2.3 ../../var/folders/sk/y7f5hkxx2cs0hzzxjdj0hx840000gn/T/tmp-6940qM9hiliHi6Nj/node_modules/gitbook
├── escape-string-regexp@1.0.5
├── escape-html@1.0.3
├── destroy@1.0.4
├── ignore@3.1.2
├── bash-color@0.0.4
├── gitbook-plugin-livereload@0.0.1
├── cp@0.2.0
├── graceful-fs@4.1.4
├── nunjucks-do@1.0.0
├── github-slugid@1.0.1
├── direction@0.1.5
├── q@1.4.1
├── spawn-cmd@0.0.2
├── gitbook-plugin-fontsettings@2.0.0
├── open@0.0.5
├── is@3.2.1
├── object-path@0.9.2
├── extend@3.0.1
├── json-schema-defaults@0.1.1
├── gitbook-plugin-search@2.2.1
├── jsonschema@1.1.0
├── crc@3.4.0
├── semver@5.1.0
├── urijs@1.18.0
├── immutable@3.8.2
├── front-matter@2.3.0
├── dom-serializer@0.1.0 (domelementtype@1.1.3, entities@1.1.1)
├── omit-keys@0.1.0 (isobject@0.2.0, array-difference@0.0.1)
├── error@7.0.2 (string-template@0.2.1, xtend@4.0.1)
├── tmp@0.0.28 (os-tmpdir@1.0.2)
├── npmi@2.0.1 (semver@4.3.6)
├── send@0.13.2 (range-parser@1.0.3, statuses@1.2.1, fresh@0.3.0, etag@1.7.0, ms@0.7.1, depd@1.1.2, mime@1.3.4, debug@2.2.0, http-errors@1.3.1, on-finished@2.3.0)
├── mkdirp@0.5.1 (minimist@0.0.8)
├── resolve@1.1.7
├── rmdir@1.2.0 (node.flow@1.2.3)
├── fresh-require@1.0.3 (is-require@0.0.1, shallow-copy@0.0.1, sleuth@0.1.1, astw@1.3.0, through2@0.6.5, escodegen@1.10.0, acorn@0.9.0)
├── gitbook-plugin-theme-default@1.0.7
├── js-yaml@3.12.0 (esprima@4.0.0, argparse@1.0.10)
├── tiny-lr@0.2.1 (parseurl@1.3.2, livereload-js@2.3.0, qs@5.1.0, debug@2.2.0, body-parser@1.14.2, faye-websocket@0.10.0)
├── cpr@1.1.1 (rimraf@2.4.5)
├── read-installed@4.0.3 (debuglog@1.0.1, util-extend@1.0.3, slide@1.1.6, readdir-scoped-modules@1.0.2, read-package-json@2.0.13)
├── gitbook-plugin-lunr@1.2.0 (html-entities@1.2.0, lunr@0.5.12)
├── gitbook-plugin-highlight@2.0.2 (highlight.js@9.2.0)
├── moment@2.13.0
├── gitbook-plugin-sharing@1.0.2 (lodash@3.10.1)
├── chokidar@1.5.0 (path-is-absolute@1.0.1, async-each@1.0.1, inherits@2.0.3, glob-parent@2.0.0, is-glob@2.0.1, is-binary-path@1.0.1, readdirp@2.1.0, anymatch@1.3.2, fsevents@1.2.4)
├── juice@2.0.0 (deep-extend@0.4.2, slick@1.12.2, batch@0.5.3, cssom@0.3.1, commander@2.9.0, cross-spawn-async@2.2.5, web-resource-inliner@2.0.0)
├── i18n-t@1.0.1 (lodash@4.17.10)
├── gitbook-markdown@1.3.2 (kramed-text-renderer@0.2.1, gitbook-html@1.3.3, kramed@0.5.6, lodash@4.17.10)
├── nunjucks@2.5.2 (asap@2.0.6, yargs@3.32.0, chokidar@1.7.0)
├── cheerio@0.20.0 (entities@1.1.1, css-select@1.2.0, htmlparser2@3.8.3, jsdom@7.2.2, lodash@4.17.10)
├── gitbook-asciidoc@1.2.2 (gitbook-html@1.3.3, asciidoctor.js@1.5.5-1, lodash@4.17.10)
├── request@2.72.0 (tunnel-agent@0.4.3, aws-sign2@0.6.0, oauth-sign@0.8.2, forever-agent@0.6.1, is-typedarray@1.0.0, caseless@0.11.0, stringstream@0.0.6, aws4@1.7.0, isstream@0.1.2, json-stringify-safe@5.0.1, tough-cookie@2.2.2, node-uuid@1.4.8, qs@6.1.2, combined-stream@1.0.6, mime-types@2.1.18, hawk@3.1.3, bl@1.1.2, http-signature@1.1.1, har-validator@2.0.6, form-data@1.0.1)
└── npm@3.9.2
GitBook version: 3.2.3

```
👆上面结果说明 在第一次执行gitbook -V 同时安装好CLI与GitBook

```
MacBook-Pro:coo$ gitbook -V
CLI version: 2.3.2
GitBook version: 3.2.3
```

>注意事项
>
> * 安装的命令前需要加入sudo,因为可能会找不到npm的 /usr/local/bin/路径。
> * 使用gitbook -v命令检查时可能会不出现版本号，但其实是安装好了。
> 
> 
> * 不能使用 npm install gitbook -g 命令安装，因为使用命令gitbook的时候会出现问题。


---
### GitBook 常用命令


##### 这里主要介绍一下 GitBook 的命令行工具 gitbook-cli 的一些命令, 首先说明两点:
> * gitbook-cli 和 gitbook 是两个软件
> * gitbook-cli 会将下载的 gitbook 的不同版本放到 ~/.gitbook中, 可以通过设置GITBOOK_DIR环境变量来指定另外的文件夹
>
>
>


列出 gitbook 所有的命令
```
MacBook-Pro:coo$ gitbook help
```

输出 gitbook-cli 的帮助信息

```
MacBook-Pro:coo$ gitbook --help
```

创建本地GitBook项目

```
MacBook-Pro:coo$ gitbook init
```


生成静态网页

```
MacBook-Pro:coo$ gitbook build
```


生成静态网页并运行服务器

```
MacBook-Pro:coo$ gitbook serve
```

生成时指定gitbook的版本, 本地没有会先下载

```
MacBook-Pro:coo$ gitbook build --gitbook=2.0.1
```

列出本地所有的gitbook版本

```
MacBook-Pro:coo$ gitbook ls
```

列出远程可用的gitbook版本

```
MacBook-Pro:coo$ gitbook ls-remote
```

安装对应的gitbook版本

```
MacBook-Pro:coo$ gitbook fetch 标签/版本号
```

更新到gitbook的最新版本

```
MacBook-Pro:coo$ gitbook update
```

卸载对应的gitbook版本

```
MacBook-Pro:coo$ gitbook uninstall 2.0.1
```

指定log的级别

```
MacBook-Pro:coo$ gitbook build --log=debug
```



输出错误信息

```
MacBook-Pro:coo$ gitbook builid --debug
```



---


#Ebook-convert 安装

#### 生成本地电子书是电子书需要安装  ebook-convert

>构建 PDF 错误：InstallRequiredError: "ebook-convert" is not installed。
>

在计算机中打开终端，执行命令

```
MacBook-Pro:coo$ sudo npm install -g ebook-convert
```
结果如下说明安装成功

```
MacBook-Pro:coo$ sudo npm install -g ebook-convert
Password:
+ ebook-convert@2.0.1
added 61 packages in 4.129s


   ╭─────────────────────────────────────╮
   │                                     │
   │   Update available 5.6.0 → 6.2.0    │
   │     Run npm i -g npm to update      │
   │                                     │
   ╰─────────────────────────────────────╯
```