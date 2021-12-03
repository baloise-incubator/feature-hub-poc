# PoC for feature toggle using [feature-hub](https://www.featurehub.io/)

`docker run -p 8085:8085 --user 999:999 -v $HOME/party:/db featurehub/party-server:latest`





## perform a repository wide search and replace for "repository-template-nosrc" and the "target-repo-name"



e.g. by using

```
cp -R repository-template-nosrc/ new-name && cd new-name && git config --local --unset remote.origin.url && git config --local --add remote.origin.url git@github.com:baloise/new-name.git && git reset --hard $(git commit-tree FETCH_HEAD^{tree} -m "Initial contribution") &&  git grep -l 'repository-template-nosrc' | xargs sed -i '' -e 's/repository-template-nosrc/new-name/g' && git add -A && git commit -m "Rename from template to new-name" && cd ..
```
[![Gitpod ready-to-code](https://img.shields.io/badge/Gitpod-ready--to--code-blue?logo=gitpod)](https://gitpod.io#https://github.com/baloise/repository-template-nosrc)

## the [docs](docs/index.md)
