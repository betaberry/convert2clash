# convert2clash
本项目fork自https://github.com/celetor/convert2clash

用作学习交流。

基本没上啥改动，主要修改了rule.yaml(原来叫config.yaml)，加了一个自动选最快的proxy-group，并删掉了冗余的部分。

## 原理
核心在于clash的配置文件config.yaml。

其中有2个的重要的配置：proxy和rule

proxy就是机场代理的ip地址，这个需要你提供订阅地址来得到。

rule就是哪些网站要用代理，哪些网站不用。

proxy + rule = 最终的config.yaml



## 使用说明:
 1. 执行pip install -r requirements.txt
 2. 创建一个文件`sub_url.txt`，把你的订阅地址放在里面（多个地址;隔开）
 3. 在`output_path.txt`文件中把你想要输出的配置文件的路径写好（多个路径请换行）
 4. （可选）有时候request可能访问不了订阅地址，所以我们需要在自己电脑上先访问一下订阅地址，把得到的内容放进去，同时需要创建一个文件`base64.txt`，把订阅地址对应的内容放进去。
 5. 执行python Robot.py
