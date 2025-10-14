# Comandos Principales de GitHub

Este documento contiene los 10 comandos más importantes de GitHub CLI y Git para trabajar con repositorios de GitHub.

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

---
*Creado por: Sebastián Córdoba - DevOps Engineer*