# 包的简介
`包(package)`可以让我们使用别人经过优化、调试的代码，[避免浪费时间](https://www.zhihu.com/question/407370305)，例如[DataStructures.jl](https://github.com/JuliaCollections/DataStructures.jl)提供了各种常见的数据结构\
包被安装后，可以以[模块](../advanced/module.md)形式使用\
在REPL中输入`]`，进入`包管理器(Pkg-REPL)`模式，可以输入`help`获取帮助\
常用指令有
* `add`下载包（第一次会下载所有注册包的状态，可能比较慢）
* `remove`移除包
* `update`更新包
* `gc`回收包
* `preview`预览

基础示例
```jl
(@v1.6) pkg> add LightLearn # 下载包
...
Precompiling project...
  1 dependency successfully precompiled in 7 seconds (173 already precompiled)

julia> using LightLearn # 导入

julia> init() # 使用
```

也可以在程序中使用[Pkg](pkg.md)
```jl
import Pkg
Pkg.add(PackageSpec(name="Example", version="0.3.1"))
```

## 包查找
* [juliahub](https://juliahub.com/lp/)
* [juliaobserver](https://juliaobserver.com/packages)
* [svaksha - 按领域分类](https://svaksha.github.io/Julia.jl/)
* [classify](classify.md)

## 包服务器
对于1.5.0以上，会默认使用[官方服务器](https://pkg.julialang.org)
对于国内用户，`https://pkg.julialang.org` 会自动导向北京、上海或者广州的服务器（状态见[此](https://status.julialang.org/)），可以通过修改环境变量`JULIA_PKG_SERVER`修改默认服务器 [详情](https://discourse.juliacn.com/t/topic/2969)

## 其它
[包开发](develop.md)

[^1]: https://pkgdocs.julialang.org/v1/
[^2]: https://discourse.juliacn.com/t/topic/2969
