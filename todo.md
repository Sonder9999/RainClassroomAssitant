https://github.com/TrickyDeath/RainClassroomAssitant 这个版本现在已经不能用了,
帮我写一个检测到题目之后自动将题目的截图通过deepseek或者其他的api来回答问题,传回后自动回答
https://github.com/zhangchi2004/THU-Yuketang-Helper 可参考这个
1.api配置要用单独的toml进行,方便我更换

2.如果用api直接发送图片困难的话,可以考虑先使用图片转文字,再发送给ai(图片转文字可以使用本地的也可以使用网上的),但是请先帮我写一版不使用图片转文字的让我试试效果(图片转文字的放在注释里就行,说明使用方法)

3.我可能会更多的使用deepseek的api以及也可能使用硅基流动的api(里面我看有图片转文字的api),例如,这是我的另一个项目,不同模块调用不同的api

[model.llm_normal]
name = "Pro/deepseek-ai/DeepSeek-V3"
provider = "SILICONFLOW"
pri_in = 2
pri_out = 8
temp = 0.2

[model.vlm]
name = "Pro/Qwen/Qwen2.5-VL-7B-Instruct"
provider = "SILICONFLOW"
pri_in = 0.35
pri_out = 0.35

[model.llm_tool_use]
name = "Qwen/Qwen2.5-32B-Instruct"
provider = "SILICONFLOW"
pri_in = 1.26
pri_out = 1.26

上面是我的需求.
https://github.com/Sonder9999/RainClassroomAssitant 这是我修改的代码,请帮我检查代码,
不知道为什么我的代码新加的功能无法实现,没有办法保存题目的截图,也没有办法询问ai问题,
甚至原来的题目的语音提醒功能也不能使用了

视觉使用Qwen/Qwen2.5-VL-72B-Instruct
分要求慢慢实现
