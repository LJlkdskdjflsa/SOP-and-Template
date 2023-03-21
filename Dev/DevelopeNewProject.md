# Develope New Project

- 從 https://github.com/xrex-inc/template-repo 建立新專案
- 使用 PyCharm 建立 fastAPI 專案,在專案中
- 加入 submodule: [docs](https://www.notion.so/xrexuiux/Goose-92eb0e2aa4c6495e946a339ce1bad6f5) Initial Goose In New Repo 部分
  - git submodule add git@github.com:xrex-inc/dev-tools.git xdev/dev-tools
- Docs
  - 
## DB setup

### Goose

#### Initial Goose In New Repo
```
git submodule add git@github.com:xrex-inc/dev-tools.git xdev/dev-tools
// it will be generate .gitmodules file and generate the information about the module
```

add `goosedb.sh` file in xdev (remember to replace DB_NAME in the below)
```
#!/bin/bash

SCRIPTPATH="xdev/dev-tools"
SCRIPTNAME="goose/goosedb.sh"
BRANCH="main"
export ARGS="$@"
export DB_NAME=NEED_TO_REPLACE

self_update() {
    cd $SCRIPTPATH
    git fetch
    git diff --name-only origin/$BRANCH | grep $SCRIPTNAME

    [ $(git diff --name-only origin/$BRANCH | grep $SCRIPTNAME) ] && {
        echo "Found a new version of me, updating myself..."
        git pull --force
        git checkout $BRANCH
        git pull --force
        echo "Already the latest version."
    }
}

main() {
    echo "Running"
    exec $SCRIPTNAME $ARGS
}

self_update
main
```

#### Create SQL query
##### Schema

`./root-path/xdev/schema`

##### Seed

`./root-path/xdev/seed`

##### mysql command
```shell
# pull the latest goose shell in your repo project
git submodule update --init --recursive

# Reset DB
sh xdev/goosedb.sh -e local -c drop

# Creates new migration file
sh xdev/goosedb.sh -e local -c create -n test_data

# Migration schema(Second use this script to update status)
sh xdev/goosedb.sh -e local -c migrate
# Migration seded(Second use this script to update status)
sh xdev/goosedb.sh -e local -c seed

# Roll back the version by 1
sh xdev/goosedb.sh -e local -c rollback

# Dump the migration status for the current DB(See the status first)
sh xdev/goosedb.sh -e local -c status
```

R:
https://github.com/pressly/goose

poetry add -D pytest pytest-cov autoflake flake8 mypy isort pre-commit pyright black SQLAlchemy-Utils pytest-xdist pytest-rerunfailures pytest-timeout sqlalchemy-stubs pytest-clarity pytest-asyncio types-requests types-pyyaml pytest-mock