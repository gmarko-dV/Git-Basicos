# 📘 Guía rápida y super básica de Git

Apuntes básicos para recordar los comandos más usados en Git por mi.

---

## Configuración Inicial🔖

```bash
git config --global user.name "gmarko-dV"
git config --global user.email "gian.pasco@tecsup.edu.pe"
git config --list   # Ver configuración
```

## 📂 Empezar un repositorio

```bash
git init               # Inicializa un repo en la carpeta actual
git clone "URL"         # Clona un repo remoto
```
## 📄 Ciclo básico
```bash
git status              # Ver estado de archivos
git add archivo.txt     # Agregar un archivo al área de staging
git add .               # Agregar todos los archivos
git commit -m "mensaje" # Guardar cambios
```
## 🔄 Ramas
```bash
git branch              # Listar ramas
git branch nueva-rama   # Crear nueva rama
git checkout nueva-rama # Cambiar a la rama
git checkout -b nueva   # Crear y cambiar a la vez
git merge ramaX         # Unir ramaX a la actual
```
## ☁️ Repositorio remoto
```bash
git remote add origin URL      # Vincular repo local con remoto
git remote -v                  # Ver remotos
git push -u origin main        # Subir cambios a remoto
git pull origin main           # Bajar cambios del remoto
git fetch                      # Descargar cambios sin mezclar
```

## ✍️ Tip: si te sale un editor como vim al hacer un commit o merge, puedes salir con:

- ESC + :q! (salir sin guardar)

- ESC + :wq (guardar y salir)


# 🔑 Guía: Usar Token de GitHub para subir proyectos

Cuando estoy en una PC que no es la mía, no uso mi clave SSH, sino un **Token de Acceso Personal (PAT)**.  
Aquí están los pasos para configurar y subir proyectos con Git y token.

---

## 1️⃣ Generar Token Classic en GitHub

1. Ir a 👉 [https://github.com/settings/tokens](https://github.com/settings/tokens).  
2. Clic en **Generate new token (classic)**.  
3. Seleccionar:
   - ✅ `repo` (para tener permisos de lectura/escritura en repos privados y públicos).  
4. Opcional: poner fecha de expiración (ej. 30 días si es temporal).  
5. Copiar el token generado.
   
## ⚠️ Cuando ejecutes el git push, la terminal pedirá:
```bash
Username for 'https://github.com':  " gmarko-dV "
Password for 'https://github.com':
```
- Username → escribe tu usuario de GitHub.

- Password → pega tu token (no tu contraseña real).

👉 Importante: cuando pegues el token, no se verá en pantalla (por seguridad), solo presiona Enter.

✅ Con esto ya puedes clonar, commitear y pushear desde cualquier PC usando tu token Classic.
