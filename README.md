# PackageApplication

`PackageApplication`已经从Xcode的工具链中移除，建议使用`xcodebuild -exportArchive`替代。

留着它在这里是为了满足两个需求：

1. 配合`xcodebuild build`使用增量编译，生成.app之后使用`PackageApplication`产生测试的ipa包。
2. 理解Apple在对ipa处理过程中的的内部细节。

这里的脚本还修复了一个BUG：

1. -o参数不能指定相对目录
