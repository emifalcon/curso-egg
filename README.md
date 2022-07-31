# curso-egg
Trabajos/Ejercicios de curso de programacion desde cero
Algoritmo EjercicioCooperativo3
		//Vamos a programar una calculadora de materiales para construir
		//Primero leeremos todo el ejercicio y luego dividiremos tareas en el equipo
	Definir variableOpcion Como Caracter
	Definir largo, ancho, esp, sup, volumen, alto como real
	Escribir "Ingrese el numero de opción que desea utilizar: " 
	Escribir "1 - Calcular muro de ladrillo"
	Escribir "2 - Calcular viga de hormigón"
	Escribir "3 - Calcular columnas de hormigón"
	Escribir "4 - Calcular contrapisos"
	Escribir "5 - Calcular techo"
	Escribir "6 - Calcular pisos"
	Escribir "7 - Calcular pintura"
	Escribir "8 - Calcular iluminación"
	Escribir "9 - Salir"
	Leer variableOpcion
		
	Segun variableOpcion Hacer
		"1": calcularMuro(largo, ancho)
//		"2": calcularViga
//		"3" calcularColumna
//		"4" calcularContrapisos
//		"5" calcularTecho
//		"6" calcularPisos
//		"7" calcularPintura
//		"8" calcularIluminacion
//		"9" salir 
//			
	FinSegun

FinAlgoritmo

Funcion retorno <- calcularSuperficie(largo Por Referencia, ancho Por Referencia)
	Definir sup Como Real
	sup = largo * ancho
Fin Funcion
 
Funcion retorno <- calcularVolumen(largo por referencia, ancho por referencia, alto por referencia)
	Definir vol Como Real
	vol = largo * ancho * alto
Fin Funcion

SubProceso calcularMuro (largo por referencia, ancho por referencia)
	Definir sup, esp, cemento, arena, ladrillos Como Real
	Escribir "Ingrese si el muro será de 20cm. o de 30cm. de espesor: "
	Leer esp
	Escribir "Ingrese el largo del muro: "
	Leer largo
	Escribir "Ingrese el alto del muro: "
	Leer ancho
	sup= calcularSuperficie(largo, ancho)
	Si esp=20 Entonces
		cemento= sup*10.9 
		Escribir  "Cemento: " cemento " kg." 
		arena= sup*0.09
		Escribir "Arena: " arena " m3."
		ladrillos= sup*90
		Escribir "Ladrillos: " ladrillos 
	SiNo
		cemento=sup*15.2
		Escribir  "Cemento: " cemento " kg." 
		arena=sup*0.115
		Escribir "Arena: " arena " m3."
		ladrillos=sup*120
		Escribir "Ladrillos: " ladrillos 
	FinSi
	
	
FinSubProceso
