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

## submodule 删除单个子模块
```
git submodule deinit -f mtxlib
rm -rf .git/modules/mtxlib
git rm -f packages/mtxlib
```
## 用重基的方式永久删除一个文件.优点,干劲利落的重建了仓库,缺点是比较危险,会重写历史,而且需要重新拉取仓库
```
git filter-branch --force --index-filter \
  'git rm --cached --ignore-unmatch packages/gomtm-cli/bin/gomtm' \
  --prune-empty --tag-name-filter cat -- --all

git push --force
```

## 用 git filter-repo 的方式永久删除一个文件
``` bash
pip install git-filter-repo
# 删除单个文件
git filter-repo --path 文件路径 --invert-paths

# 例如删除 password.txt
git filter-repo --path password.txt --invert-paths

# 删除多个文件
git filter-repo --path 文件1 --path 文件2 --invert-paths

# 删除某个目录
git filter-repo --path-glob '目录名/*' --invert-paths
```
