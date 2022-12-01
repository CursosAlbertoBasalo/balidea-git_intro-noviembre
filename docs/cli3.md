```bash
git log --oneline
git switch main
git log --oneline
git merge feature/1-crear-index-html
git log --oneline
# meter un cambio en el index.html
git add -A
git commit -m "docs: placeholder para la lista"
git switch feature/1-crear-index-html
# meter un cambio en el index.html
git add -A
git commit -m "feat: cabecera de listado"
git switch main
git merge feature/1-crear-index-html
# Arreglar el conflicto eliminando el placeholder
git add -A
git commit -m "feat: eliminar placeholder"
git branch -d feature/1-crear-index-html



# stash
# nueva feature crear listado de actividades
git checkout -b feature/2-listado-actividades
# mientras lo creamos aparece fix de pone los meta en el head
git stash
git checkout main
git checkout -b fix/3-metas-head
# modificar el index html
git commit -a -m "fix: add metas to head"
git switch main
git merge fix/3-metas-head
git switch feature/2-listado-actividades
git merge main
git stash apply
# termino la modificación
git commit -a -m "feat: listado actividades"
# mezclo en main
git switch main
git merge feature/2-listado-actividades
git branch
git branch -d feature/2-listado-actividades
git branch -d fix/3-metas-head
git log --graph --oneline

# tags
git tag sprint-1
git tag
git log --graph --oneline
git checkout d41da13
git checkout sprint-1
git checkout main
```
