## 五笔98 Rime输入法Mac配置 Mac OS 14测试

备份的码表等配置文件

> 注：根据这位资深程序员的 Gist 修改而成 https://gist.github.com/agentzh/6b734548505c07341ea3

## 安装

下载 <a href="https://rime.im/" target="_blank">鼠须管</a>，安装后会注销当前账户，然后去键盘-输入法里面添加鼠须管

## 备份初始配置（可选）

防止操作不当配置无法恢复，可以为初始配置做个备份。在【终端】中输入以下命令，按回车键，会出现一个【Rime.bak】文件夹即备份。

```
cp -r ~/Library/Rime ~/Library/Rime.bak
```

![](https://i.imgur.com/1EFPjAK.png)

> 还原：初始配置【Rime】文件夹清空，将【Rime.bak】内的文件复制粘贴过去，点击菜单栏【ㄓ】-【重新部署】。


## 定制

1. Rime 五笔98输入法的配置。将下列文件拷贝到 Rime 配置目录（在 Mac OS X 上为 ~/Library/Rime/），然后点击屏幕右上角输入法的 Rime 图标，在出现的输入法菜单中点击 Deloy（或“布署”）菜单项即可生效。
2. Rime 官方提供的五笔 86 输入法的配置并不会四码自动上屏（无重码时），
需要在 .schema.yaml 配置文件里的 speller 段落下添加 max_code_length: 4 和 auto_select: true 这两行就可以了。这是一个小坑，貌似只在官方更新日志里提及了。其他的在官方手册里讲得很详细。很赞。
3. Rime 官方提供的五笔 86 的码表里的字频权重，继承到我自己的 98 码表里，这样重码的默认排序就比较人性了。
