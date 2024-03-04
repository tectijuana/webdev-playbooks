# django-playbook

Este repositorio contiene un script de Ansible diseñado para configurar automáticamente un entorno de desarrollo Django en una máquina remota. Actualmente, está optimizado para funcionar en sistemas Ubuntu 22.04.

## Características Incluidas:
- **nvim** como editor de código.
- **PostgreSQL** como sistema de gestión de bases de datos.

## Tareas Pendientes:
- Clonación de un repositorio de Django desde GitHub.
- Creación de un entorno virtual y la instalación de las dependencias necesarias.

El script está configurado, por ahora, para ejecutarse en el servidor de desarrollo proporcionado por Django.

## Uso en GitHub Codespaces:

1. **Inicialización**: Abre este repositorio en un Codespace.
2. **Configuración de la Llave SSH**:
   - Sube tu archivo de llave SSH al directorio `ssh-keys`. Para ello, haz clic derecho en el directorio `ssh-keys` en el explorador de archivos y selecciona la opción "Upload...".
   - Cambia los permisos del archivo de llave ejecutando el comando `chmod 400 ssh-keys/tu-llave.pem` en la terminal.
3. **Instalación de Ansible**: Ejecuta `pip install ansible` para instalar Ansible.
4. **Configuración del Host**:
   - Añade la información de tu host y llave SSH al archivo `hosts.yml`.
5. **Ejecución del Playbook**:
   - Para configurar tu entorno, ejecuta el playbook deseado. Por ejemplo, para configurar PostgreSQL, usa el comando `ansible-playbook playbooks/postgres.yml -i hosts.yml`.

Este flujo de trabajo simplifica la configuración inicial de tu entorno de desarrollo Django en una máquina remota, aprovechando las capacidades de automatización de Ansible y la flexibilidad de GitHub Codespaces para un desarrollo más ágil y sin contratiempos.
