# 通用 CRUD

## 简单介绍

TODO

> 实体无注解化设置，表字段如下规则，主键叫 id 可无注解大写小如下规则。

1、驼峰命名 【 无需处理 】 

2、全局配置： 下划线命名 dbColumnUnderline 设置 true ,  大写 isCapitalMode 设置 true


## 注解说明

> 表名注解 `@TableName`

- com.baomidou.mybatisplus.annotations.TableName

值                | 描述
---------------- | ---------------------
value            | 表名（ 默认空 ）
resultMap        | xml 字段映射 resultMap ID


> 主键注解 `@TableId `

- com.baomidou.mybatisplus.annotations.TableId

值                | 描述
---------------- | ---------------------
value            | 字段值（驼峰命名方式，该值可无）
type             | 主键 ID 策略类型（ 默认 INPUT ，全局开启的是 ID_WORKER ）

!> 暂不支持组合主键


> 字段注解 `@TableField `

- com.baomidou.mybatisplus.annotations.TableField

值                | 描述
---------------- | ---------------------
value            | 字段值（驼峰命名方式，该值可无）
el               | 详看注释说明
exist            | 是否为数据库表字段（ 默认 true 存在，false 不存在 ）
strategy         | 字段验证 （ 默认 非 null 判断，查看 com.baomidou.mybatisplus.enums.FieldStrategy ）
fill             | 字段填充标记 （ FieldFill, 配合自动填充使用 ）

- 字段填充策略 FieldFill

值                | 描述
---------------- | ---------------------
DEFAULT | 默认不处理
INSERT | 插入填充字段
UPDATE | 更新填充字段
INSERT_UPDATE | 插入和更新填充字段



> 序列主键策略 注解 `@KeySequence `

- com.baomidou.mybatisplus.annotations.KeySequence

值                | 描述
---------------- | ---------------------
value            | 序列名
clazz            | id的类型


> 乐观锁标记注解 `@Version `

- com.baomidou.mybatisplus.annotations.Version

!> 排除非表字段、查看文档常见问题部分！

