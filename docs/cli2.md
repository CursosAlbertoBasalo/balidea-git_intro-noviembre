```bash
# modify readme.md agregar autor
git add -A
git status
git commit -m "docs: agregar autor"
git status
git log
# time travel
git checkout [COMMIT_HASH]
git log
git status
# travel back to head
git checkout -
# travel back to past
git checkout -
# change something and restore
git restore .\README.md
git checkout main
# change readme and commit agregar fecha al autor
git commit -a -m "agregar fecha al autor"
git log
git commit --amend -m "docs: agregar fecha al autor"
git log
# change readme (bad) and commit agregar enlace del autor

git commit -a -m "docs: agregar enlace del autor"
# change readme (good) and commit agregar enlace del autor
git add -A
git commit --amend --no-edit
git log

# git config --global core.editor "code -w"
# git config --global core.editor "C:\Users\alber\AppData\Local\Programs\Microsoft VS Code\bin\code"
# rebase commits
git rebase -i HEAD~3
# p s s
git log
git log --oneline

# feature branch
git branch
git branch feature/1-crear-index-html
git status
git branch
git switch feature/1-crear-index-html
# crear index.html con titulo
git add -A
git commit -m "feat: crear index.html con título"
git log --oneline
```
