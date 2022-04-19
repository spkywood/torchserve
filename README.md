# torchserve

##### 模型打包，等同于 `torch-model-archiver`

```shell
zip -r ../mymodel.mar ./
```

##### 目录结构

```shell
./
├── config.properties
├── MAR-INF/
│   └── MANIFEST.json
├── model_handler.py
├── model.pt
├── model_store/
└── README.md
```

`model_store` 存放打包模型

##### torchserve


###### start

```
torchserve --start --model-store model_store --models mymodel=mymodel.mar --ts-config ./config.properties
```

###### stop

```
torchserve --stop
```