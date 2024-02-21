# Lightweight-Fine-Tuning-Project

you need to specify the task type in Lora's configuration
```
from peft import LoraConfig, TaskType
config = LoraConfig(target_modules=["classifier"], task_type=TaskType.SEQ_CLS, r=8, lora_alpha=16)
```
and due to the low amount of training data, you need to add logging_steps=100 to training arguments

and I recommend checking this topic about Lora configurations

https://medium.com/@manyi.yim/more-about-loraconfig-from-peft-581cf54643db
