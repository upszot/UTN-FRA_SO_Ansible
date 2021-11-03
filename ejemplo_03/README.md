# Ansible - Ejemplo 03

	- La finalidad del ejemplo 03 es explicar la estructura de directorios.

  

## Precondiciones:
	- Tener instalado ansible

## Ejecucion del playbook de testing del rol:
```
ansible-playbook -i tests/inventory tests/test.yml
```
### Contenido:
	- Carpeta "role_ejemplo1" -> es un rol que imprime un hola mundo
    	- carpeta test -> inventario y playbook (test.yml) 
    	- ansible.cfg -> Agregado a mano donde se define:
        	-  Paths donde tiene que buscar los roles
        	-  Path donde quedan los logs de ejecucion del playbook, etc.

## Ejercitacion Para el Alumno:
	- El alumno debe generar la siguiente estructura de directorios:
    	- $HOME/repo_ansible/
  	- Crear 1 playbook desde donde se invocaran los roles:
    	-  $HOME/repo_ansible/practica_playbook/
    	-  Dentro de dicha carpeta debe existir los archivos playbook.yml, ansible.cfg, inventory
	- Inicializar un rol de ansible (Estando en $HOME/repo_ansible/) con el siguiente comando.
```
ansible-galaxy role init rol_ejemplo1
```
		- Agregar en tasks/main.yml una tarea "mensaje hola desde el rol"
    	- Editar el playbook e inventory de test dentro de la carpeta test (Generalmente usado para CI)
    - Editar en $HOME/repo_ansible/practica_playbook/   Los archivos:
      - playbook.ym incluir el rol
      - inventory  definir listado de host

	- Pruebas de Funcionamiento:
    	- Realizar una prueba de ejecucion desde el playbook de testing del rol (validar rol)
    	- Realizar una prueba de ejecucion desde el playbook de la receta "practica_playbook"

