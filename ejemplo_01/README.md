# Ansible - Ejemplo Playbook 01

	- Playbook basico estilo "Hola mundo".

## Precondiciones:
	- Tener instalado ansible

## Ejecucion:
```
ansible-playbook -i inventory playbook.yml
```

### Contenido:
	- playbook.yml  -> receta (con 2 tareas)
	- inventory  -> inventario escrito en formato INI
	- ansible.cfg -> configuracion local de ansible

### Comportamiento:
	- Tareas Implicitas: recolecta facts
	- Tarea1: Imprime "Ejemplo de playbook - 01"  
    	- 2 veces (ya que en un host no se va a poder conectar)
	- Tarea2: Imprime:
		- Nombre de equipo
		- Grupo del inventario al que pertenece

## Documentarion relacionada:
```
ansible-doc debug
```

facts and magic variables
https://docs.ansible.com/ansible/latest/user_guide/playbooks_vars_facts.html


