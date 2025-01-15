# 备忘
## 当主项目提交子模块的文件更新而github.com上看不到更新的结果时,可能因为不知道什么原因让子模块的分支没有正确挂钩到主分支
解决方式
```
<!-- git submodule sync -->
<!-- 重新checkout main分支 -->
cd packages/mtmaiui && git checkout main

```

## submodule 操作技巧备忘
```bash
# 克隆主项目时直接初始化所有子模块
git clone --recurse-submodules YOUR_PRIVATE_REPO_URL

# 或者在已有项目中一次性初始化所有子模块
git submodule update --init --recursive

# 拉取所有子模块的最新代码
git submodule update --remote --merge

```
