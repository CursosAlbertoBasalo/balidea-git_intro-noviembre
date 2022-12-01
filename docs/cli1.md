```bash
mkdir balidea-git
cd balidea-git
git init
git status
# creare readme.md with content
git add .\README.md
git status
git commit -m "docs: agregar el read me"
git status
git log
git cat-file [COMMIT_HASH] -t
git cat-file [COMMIT_HASH] -p
git cat-file [COMMIT_TREE] -t
git cat-file [COMMIT_TREE] -p
git cat-file [COMMIT_BLOB] -t
git cat-file [COMMIT_BLOB] -p
```
