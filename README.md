# GitHub
Codigos básicos para la terminal

# 1. Instalar Git
sudo apt update
sudo apt install git

# 2. Configurar tu nombre de usuario y correo electrónico en Git
git config --global user.name "TuNombreDeUsuario"
git config --global user.email "tuemail@ejemplo.com"

# 3. Verificar la configuración actual de Git
git config --list

# 4. Generar una clave SSH para conectarte a GitHub
ssh-keygen -t rsa -b 4096 -C "tuemail@ejemplo.com"

# 5. Iniciar el agente SSH
eval "$(ssh-agent -s)"

# 6. Añadir la clave privada generada al agente SSH
ssh-add ~/.ssh/id_rsa

# 7. Mostrar la clave pública para añadirla a GitHub
cat ~/.ssh/id_rsa.pub

# (A continuación, copia y pega la clave pública mostrada en tu perfil de GitHub)

# 8. Clonar un repositorio remoto de GitHub a tu máquina local
git clone git@github.com:TuUsuario/TuRepositorio.git

# 9. Crear un nuevo repositorio en tu máquina local
git init NombreDelRepositorio

# 10. Añadir archivos al repositorio
cd NombreDelRepositorio
git add .

# 11. Confirmar los cambios (commit)
git commit -m "Mensaje del commit"

# 12. Vincular tu repositorio local con el repositorio remoto de GitHub
git remote add origin git@github.com:TuUsuario/TuRepositorio.git

# 13. Subir (push) los cambios al repositorio remoto
git push -u origin master

# 14. Ver el estado del repositorio
git status

# 15. Actualizar el repositorio local con los cambios del remoto
git pull origin master

# 16. Ver el historial de commits
git log
