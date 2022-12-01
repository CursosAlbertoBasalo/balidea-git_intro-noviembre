```bash
# rebase gitflow

git checkout main # rama en producción
git checkout -b develop # rama de integración de código
# Fase de desarrollo
git checkout -b feature/4-activity-pages # rama desarrollo local
git commit -a -m "feat: add activity page"
git commit -a -m "feat: add links to activity pages"
git rebase -i HEAD~2 # rebase interactivo de los últimos commits para tener uno solo
git fetch # traer cambios de remoto
git rebase origin/develop # rebase de la rama local con la remota
# resolver conflictos
git push -u origin feature/4-activity-pages # subir rama local a remota
# pedir integración a responsable de la rama develop
git checkout develop # nos movemos a la rama de integración
git rebase feature/4-activity-pages # rebase de la rama de integración con la rama funcional
# Fase de pruebas
get checkout -b release/sprint-2 # rama de preparación de la versión
git merge develop # mezclar la rama de integración con la rama de preparación
# si todo va bien (o se ha resuelto el problema)
# Fase de despliegue
git checkout develop # volvemos a la rama de integración
git merge release/sprint-2 # mezclamos la rama de preparación con la de integración
git checkout main # nos movemos a la rama de producción
git merge develop # mezclamos la rama de desarrollo con la rama de producción
# Fase de etiquetado y limpieza
git tag -a v2.0.0 -m "chore: release sprint 2" # creamos una etiqueta para la versión
git branch -d feature_branch # eliminamos nuestra rama funcional
git push origin -d feature_branch # eliminamos la rama funcional en remoto
git reflog # ver el historial de commits

# alias

code "C:\Users\[USER_NAME]\.gitconfig"

[alias]
  co = checkout
  ci = commit
  ma = checkout main
  st = !git fetch && git branch -vv && git status
  lg = log --color --graph --pretty --abbrev-commit --branches
  lgp = log --color --graph --pretty=format:'%Cred%h%Creset -%C(yellow)%d%Creset %s %Cgreen(%cr) %C(bold blue)<%an>%Creset' --abbrev-commit --branches
```
