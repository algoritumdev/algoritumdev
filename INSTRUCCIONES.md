# Cómo poner esto en tu perfil

## 1. Crear el repositorio

GitHub muestra en tu perfil el README de un repositorio que se llame **exactamente
igual que tu usuario**. En tu caso:

```
Benji69-codemaster
```

Entrá a https://github.com/new y creá el repo con ese nombre exacto.
Tiene que ser **público** y **bajo tu cuenta personal**, no bajo la organización
`algoritumdev` — los perfiles no leen repos de organizaciones.

No marques "Add a README": el que va ya está en este zip.

## 2. Subir los archivos

En Git Bash, un comando por línea:

```
powershell -c 'Expand-Archive "C:\Users\denis\Downloads\algoritum-perfil.zip" "C:\Users\denis\Downloads\perfil" -Force'
```

```
cd ~/Downloads/perfil/perfil
```

```
git init && git branch -M main
```

```
git remote add origin https://github.com/Benji69-codemaster/Benji69-codemaster.git
```

```
git add . && git commit -m "Perfil ALGORITUM"
```

```
git push -u origin main
```

## 3. Encender la serpiente

La serpiente no aparece sola la primera vez: la genera una GitHub Action.

1. Entrá al repo → pestaña **Actions**
2. Si pide confirmación para habilitar workflows, aceptá
3. En la lista de la izquierda elegí **serpiente**
4. Botón **Run workflow** → **Run workflow**

Tarda menos de un minuto. Cuando termine, se crea sola una rama `output` con el
SVG adentro. Recargá tu perfil y ya está.

De ahí en adelante se regenera sola todos los días a las 6 de la mañana UTC.

## Si algo no aparece

**La serpiente sale rota** → la Action todavía no corrió, o falló. Miralo en la
pestaña Actions.

**Las estadísticas salen en blanco** → el servicio público de
`github-readme-stats` a veces se queda sin cupo de la API de GitHub. Suele
volver en minutos. Si te pasa seguido, se puede montar tu propia instancia en
Vercel y cambiar la URL del README.

**El retrato no se mueve** → GitHub cachea las imágenes. Probá en una ventana de
incógnito antes de dar por perdido nada.

## Qué tocar si querés cambiar cosas

El texto del panel está en `assets/panel.svg`, pero conviene no editarlo a mano:
está generado. Si querés cambiar el contenido, pedímelo y te lo regenero.

El texto del README es markdown común: editalo directo.
