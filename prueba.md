

# Introducción y pasos iniciales
doc.add_paragraph("""
Para subir un archivo a GitHub utilizando Git Bash, sigue los siguientes pasos:
""")

# Paso 1: Crear un repositorio en GitHub
doc.add_heading('1. Crea un repositorio en GitHub', level=1)
doc.add_paragraph("""
1. Ve a GitHub y accede a tu cuenta.
2. Haz clic en el botón de "New" o "Crear repositorio" para crear un nuevo repositorio.
3. Nombra tu repositorio, decide si quieres que sea público o privado y si deseas añadir un archivo README.md o .gitignore (esto es opcional).
4. Haz clic en "Create repository" para crear tu repositorio.
""")

# Paso 2: Configurar Git
doc.add_heading('2. Configura Git en tu máquina', level=1)
doc.add_paragraph("""
Si es la primera vez que usas Git en tu máquina, debes configurarlo de la siguiente manera:
""")
doc.add_paragraph("""
1. Abre Git Bash.
2. Configura tu nombre de usuario:
   git config --global user.name "Tu Nombre"
3. Configura tu correo electrónico (debe ser el mismo con el que te registraste en GitHub):
   git config --global user.email "tuemail@example.com"
""")

# Paso 3: Inicializar repositorio local
doc.add_heading('3. Inicializa un repositorio Git localmente', level=1)
doc.add_paragraph("""
1. Abre Git Bash en la carpeta donde está tu proyecto. Si no estás en la carpeta correcta, navega hacia ella con:
   cd ruta/de/tu/proyecto
2. Inicializa el repositorio local con:
   git init
""")

# Paso 4: Añadir archivos al repositorio
doc.add_heading('4. Añadir archivos al repositorio', level=1)
doc.add_paragraph("""
1. Añade los archivos que quieres subir al repositorio:
   git add nombre_del_archivo
2. Para añadir todos los archivos a la vez, usa:
   git add .
""")

# Paso 5: Hacer commit
doc.add_heading('5. Haz un commit', level=1)
doc.add_paragraph("""
Haz un commit para confirmar los cambios añadidos con el siguiente comando:
   git commit -m "Descripción del cambio"
""")

# Paso 6: Conectar repositorio local con el repositorio en GitHub
doc.add_heading('6. Conectar el repositorio local con el repositorio en GitHub', level=1)
doc.add_paragraph("""
1. Ve a tu repositorio en GitHub y copia la URL (puede ser HTTPS o SSH).
2. Vuelve a Git Bash y enlaza tu repositorio local con el remoto en GitHub usando la URL copiada. Ejemplo usando HTTPS:
   git remote add origin https://github.com/tu_usuario/nombre_del_repositorio.git
""")
doc.add_paragraph("""
**Si obtienes el error: "remote origin already exists"**, esto significa que ya existe una conexión remota configurada. Puedes:
- Modificar la URL existente con:
  git remote set-url origin https://github.com/JCEXCELSIOR/hello-world.git
- O eliminar y volver a agregar el origin:
  git remote remove origin
  git remote add origin https://github.com/JCEXCELSIOR/hello-world.git
""")

# Paso 7: Subir archivos a GitHub
doc.add_heading('7. Subir los archivos a GitHub', level=1)
doc.add_paragraph("""
Finalmente, sube los cambios al repositorio remoto con:
   git push -u origin main
""")

# Verificación de pasos adicionales
doc.add_heading('Verificaciones adicionales', level=1)
doc.add_paragraph("""
Si no ves el archivo en GitHub, verifica los siguientes pasos:

1. **Verifica que el archivo fue añadido correctamente** con el comando:
   git add nombre_del_archivo

2. **Verifica si realizaste el commit** con:
   git commit -m "Descripción del commit"

3. **Verifica si el push fue exitoso** usando:
   git push -u origin main

4. **Verifica la URL remota** con:
   git remote -v
""")

# Guardar el documento
file_path = "/mnt/data/Subir_Archivo_GitHub_GitBash.docx"
doc.save(file_path)

file_path
