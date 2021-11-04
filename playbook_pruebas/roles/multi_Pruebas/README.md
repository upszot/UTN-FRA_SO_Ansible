# Ansible - Ejemplo Rol multi_Pruebas

	- La idea es tener un ejemplo de un rol un poco mas completo
		Para poder ver la potencialidad de ansible y el uso de la estructura de directorio.

	- Uso de variables
	- Inclusion de roles
	- Inclusion de archivos


## Precondiciones:
	- Tener instalado ansible

## Ejecucion (uso normal):
```
ansible-playbook -i tests/inventory/hosts tests/test_playbook.yml
```

## Otras formas de Ejecucion:
- solo tareas con tag "otros" :
```
ansible-playbook -i tests/inventory/hosts tests/test_playbook.yml -t otros
```
- skipeando tareas con tag "cartel" :
```
ansible-playbook -i tests/inventory/hosts tests/test_playbook.yml --skip-tags cartel 
```
- Definiendo usuario contra el que se conecta (-u) y que pida clave de ssh (-k) :
```
ansible-playbook -i tests/inventory/hosts tests/test_playbook.yml -u usuario -k
```
- Solo contra 1 grupo o contra 1 host (-l) :
```
ansible-playbook -i tests/inventory/hosts tests/test_playbook.yml -l produccion
```

### Contenido:
	- playbook.yml  -> receta 
	- inventory  -> inventario escrito en formato INI
	- Carpeta file con index.html
	- ansible.cfg -> configuracion local de ansible

### Comportamiento:
	- Se conecta a todos los servidores definidos en el inventory
	- Setea variables segun grupos y hosts
	- Pide Nro de prueba
    	- De a cuerdo al Nro ingresado:
    	- Nro 1: Muestra mensaje "Dentro prueba_1"
    	- Nro 2: Muestra valores de variables segun los distintos archivos
    	- Nro 3: Crea directorios en /tmp/multi_Pruebas_borrame y deja archivo segun template

