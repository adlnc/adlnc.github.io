# adlnc.github.io

[blowfish](https://blowfish.page/)

## Commands
```sh
# install
git init
mkdir src
docker-compose run --rm hugo new site .

git submodule add https://github.com/nunocoracao/blowfish.git src/themes/blowfish
rm src/config.toml
cp src/themes/blowfish/config src/

# run
docker-compose up -d

# update
git submodule update --remote --merge

# configure
# edit src/config/_default/config.toml, languages, etc...

```

Pipeline runs `hugo --minify`
Generates static files to /docs because `src/config/_default/config.toml` has `publishDir = "./docs"`
