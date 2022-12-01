```bash
npm init -y
# gitignore .vscode node_modules
git add .\.gitignore
git commit -m "chore: add gitignore exceptions"

npm i -D standard-version
git add
git commit -a -m "chore: install and configure standard-version"

git branch release/sprint-1
git switch release/sprint-1
npm run release
git switch main
git merge release/sprint-1
git log --oneline --graph
# mirar el fichero changelog

# remotes
git remote add origin https://github.com/[USER_ORGANIZATION]/[REPO_NAME].git
git remote
git push -u origin main
git status

# agregar un fichero de licencia LICENSE en editor remoto
git status
git fetch
git diff origin/main
git diff ...origin/main
git merge
git diff origin/main
git status

# conflictos
# Hacer un cambio en le fichero de licencia en el servidor
# hacer un cambio local
git commit -a -m "chore: descripción package"
# intentar subir
git push
git status
git fetch
git diff ...origin/main
git merge
git status
git push
git status
git checkout -b release/sprint-2
npm run release
git checkout -
git tag
git push --tags

```
