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


## Robot.py中的参数 :
 1. sub_url=订阅地址（多个地址;隔开）
 2. output_path=转换成功后文件输出路径 默认输出至当前目录的config.yaml中
 3. rule_url=来自互联网的规则策略，如果失败，就进入下一步
 4. rule_path=来自本地的规则策略 默认选择当前目录的rule.yaml文件



## 使用说明:
 1. 执行pip install -r requirements.txt
 2. 创建一个文件sub_url.txt，把你的订阅地址放在里面（多个地址;隔开）
 3. 执行python Robot.py
