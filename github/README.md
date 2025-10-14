# Comandos Principales de GitHub

Este documento contiene los comandos más importantes de GitHub CLI y Git para trabajar con repositorios de GitHub.

## 1. git clone
Clona un repositorio desde GitHub a tu máquina local.
```bash
git clone https://github.com/usuario/repositorio.git
```

## 2. git add
Añade archivos al área de staging para el próximo commit.
```bash
git add archivo.txt
git add .  # Añade todos los archivos
```

## 3. git commit
Crea un commit con los cambios en el área de staging.
```bash
git commit -m "Mensaje del commit"
```

## 4. git push
Sube los commits locales al repositorio remoto en GitHub.
```bash
git push origin main
git push  # Si ya está configurado el upstream
```

## 5. git pull
Descarga y fusiona los cambios del repositorio remoto.
```bash
git pull origin main
git pull  # Si ya está configurado el upstream
```

## 6. git branch
Gestiona las ramas del repositorio.
```bash
git branch  # Lista ramas locales
git branch nueva-rama  # Crea una nueva rama
git branch -d rama  # Elimina una rama
```

## 7. git checkout / git switch
Cambia entre ramas o commits.
```bash
git checkout main
git checkout -b nueva-rama  # Crea y cambia a nueva rama
git switch main  # Comando más moderno
```

## 8. git merge
Fusiona una rama con la rama actual.
```bash
git merge feature-branch
```

## 9. git status
Muestra el estado actual del repositorio de trabajo.
```bash
git status
```

## 10. git log
Muestra el historial de commits.
```bash
git log
git log --oneline  # Versión resumida
git log --graph  # Con gráfico de ramas
```

## 🚀 Comandos Avanzados de GitHub

### 11. git rebase
Reaplica commits en una nueva base, útil para mantener un historial lineal.
```bash
git rebase main  # Rebase rama actual sobre main
git rebase -i HEAD~3  # Rebase interactivo de los últimos 3 commits
git rebase --continue  # Continúa después de resolver conflictos
git rebase --abort  # Cancela el rebase
```

### 12. git reset
Deshace cambios moviendo HEAD a un commit específico.
```bash
git reset --soft HEAD~1  # Deshace último commit, mantiene archivos staged
git reset --mixed HEAD~1  # Deshace commit y staging (por defecto)
git reset --hard HEAD~1  # Deshace todo, PELIGROSO - pérdida de datos
git reset archivo.txt  # Quita archivo del staging area
```

### 13. git stash
Guarda temporalmente cambios sin hacer commit.
```bash
git stash  # Guarda cambios actuales
git stash push -m "mensaje"  # Guarda con mensaje
git stash list  # Lista todos los stashes
git stash pop  # Aplica y elimina el último stash
git stash apply stash@{1}  # Aplica stash específico sin eliminarlo
git stash drop stash@{0}  # Elimina stash específico
```

### 14. gh repo fork
Crea un fork de un repositorio existente.
```bash
gh repo fork usuario/repositorio  # Fork de un repo
gh repo fork usuario/repositorio --clone  # Fork y clona localmente
gh repo fork --remote  # Agrega fork como remote al repo actual
```

### 15. gh release create
Crea y gestiona releases/versiones en GitHub.
```bash
gh release create v1.0.0  # Crea release
gh release create v1.0.0 --title "Versión 1.0" --notes "Changelog"
gh release create v1.0.0 archivo.zip  # Con archivos adjuntos
gh release list  # Lista releases
gh release view v1.0.0  # Ve detalles de un release
```

## Comandos Bonus de GitHub CLI

### gh repo create
Crea un nuevo repositorio en GitHub.
```bash
gh repo create nombre-repo --public
gh repo create nombre-repo --private
```

### gh pr create
Crea un pull request.
```bash
gh pr create --title "Título" --body "Descripción"
```

### gh pr merge
Fusiona un pull request.
```bash
gh pr merge numero-pr
```

### gh issue create
Crea y gestiona issues.
```bash
gh issue create --title "Bug report" --body "Descripción del bug"
gh issue list  # Lista issues
gh issue view 1  # Ve issue específico
```

### gh workflow run
Ejecuta workflows de GitHub Actions.
```bash
gh workflow list  # Lista workflows
gh workflow run deploy.yml  # Ejecuta workflow específico
gh run list  # Lista ejecuciones de workflows
```

---
*Actualizado por: Sebastián Córdoba - DevOps Engineer*