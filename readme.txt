DEPLOY TRABAJO PRÁCTICO SISTEMAS OPERATIVOS "TORTUGA MARÍTIMA"

Pasos:

1) Correr "ifconfig" para obtener ip.

2) Ingresar ip a putty

3) Correr:

git clone https://github.com/sisoputnfrba/so-deploy
cd so-deploy
./deploy.sh -r=release -p=utils -p=consola -p=cpu -p=kernel -p=memoria -p=filesystem tp-2023-1c-Tortuga-Mar-tima 


---------------------------------------------------------

*PRUEBAS:

-MEMORIA

	Base:
	bin/memoria.out config_pruebas/prueba_base

	Deadlock:
	bin/memoria.out config_pruebas/prueba_deadlock

	Memoria:
	bin/memoria.out config_pruebas/prueba_memoria

	FileSystem:
	bin/memoria.out config_pruebas/prueba_fs

	Errores:
	bin/memoria.out config_pruebas/prueba_errores



-CPU

	Base:
	bin/cpu.out config_pruebas/prueba_base

	Deadlock:
	bin/cpu.out config_pruebas/prueba_deadlock

	Memoria:
	bin/cpu.out config_pruebas/prueba_memoria

	FileSystem:
	bin/cpu.out config_pruebas/prueba_fs

	Errores:
	bin/cpu.out config_pruebas/prueba_errores

-FILESYSTEM

	Base:
	bin/filesystem.out config_pruebas/prueba_base

	Deadlock:
	bin/filesystem.out config_pruebas/prueba_deadlock

	Memoria:
	bin/filesystem.out config_pruebas/prueba_memoria

	FileSystem:
	bin/filesystem.out config_pruebas/prueba_fs

	Errores:
	bin/filesystem.out config_pruebas/prueba_errores

-KERNEL

	Base:
	bin/kernel.out config_pruebas/prueba_base

	Deadlock:
	bin/kernel.out config_pruebas/prueba_deadlock

	Memoria:
	bin/kernel.out config_pruebas/prueba_memoria

	FileSystem:
	bin/kernel.out config_pruebas/prueba_fs

	Errores:
	bin/kernel.out config_pruebas/prueba_errores

-CONSOLA

	Base:
	bin/consola.out config_pruebas/BASE_1 consola.config
	bin/consola.out config_pruebas/BASE_2 consola.config
	bin/consola.out config_pruebas/BASE_2 consola.config

	Deadlock:
	bin/consola.out config_pruebas/DEADLOCK_1 consola.config
	bin/consola.out config_pruebas/DEADLOCK_2 consola.config
	bin/consola.out config_pruebas/DEADLOCK_3 consola.config

	Esperar a que se bloqueen y despues:
	bin/consola.out config_pruebas/DEADLOCK_4 consola.config

	Memoria:
	bin/consola.out config_pruebas/MEMORIA_1 consola.config
	bin/consola.out config_pruebas/MEMORIA_2 consola.config
	bin/consola.out config_pruebas/MEMORIA_3 consola.config

	FileSystem:
	Verificar que en la config de filesystem diga formatear = 1 y ejecutar
	bin/consola.out config_pruebas/FS_1 consola.config
	bin/consola.out config_pruebas/FS_2 consola.config
	
	Esperar a que finalicen, finalizar los módulos (Entrar al archivo y poner
	formatear = 0 en la config) y ejecutar 4 consolas con:

	bin/consola.out config_pruebas/FS_3 consola.config

	Errores:
	bin/consola.out config_pruebas/ERROR_1 consola.config
	bin/consola.out config_pruebas/ERROR_2 consola.config
	bin/consola.out config_pruebas/ERROR_3 consola.config
	bin/consola.out config_pruebas/ERROR_4 consola.config
