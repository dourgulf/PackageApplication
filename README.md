# PackageApplication

`PackageApplication`已经从Xcode的工具链中移除，建议使用`xcodebuild -exportArchive`替代。
但是，最近在使用`exportArchive`的时候，却遇到了个小问题，每次`exportArchive`都要全量编译，这让平时的开发构建效率大打折扣。
而`xcodebuild build`命令则可以指定增量编译。于是，重新拿起PackageApplication。

留着这个脚本还有另外一个意义，那就是可以清楚的看到Apple在对IPA处理过程的内部操作细节。

并修复了一个BUG：

1. -o参数不能指定相对目录
