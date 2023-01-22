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
## CI
On `main` branch push, pipeline builds (runs `hugo --minify -s src`)  
Generates static files to ../public because `src/config/_default/config.toml` has `publishDir = "../public"`  
Then pushes to `gh-pages` branch which is configured to be used by GitHub Pages (Settings>Pages>Branch)  
