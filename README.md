# hugo-vrcoder

更新网站步骤：

1. 添加或修改相应post或page文件；
2. hugo & hugo server，本地测试 确认无误；
3. rm -rf public
4. git submodule add -b master -f git@github.com:vrcoder/vrcoder.github.io.git public 
5. hugo
6. 按如下步骤更新
cd public
git add -A

msg="rebuilding site `date`"
if [ $# -eq 1  ]
  then msg="$1"
fi
git commit -m "$msg"

git push origin master
