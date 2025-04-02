# ProyectoM2
Aprendiendo a Programar en Python
################## Frase ################## En este proyecto el usuario ingresara una frase la que ella quiera para el que el programa determine la cantidad de letras que contiene.
#El usuario podra elegir una opción determinada 1 para ingresar la frase o 2 para concluir el programa.
while True:
    opcion = input("\nIngrese la opción: (1) Ingresar frase / (2) Terminar: ")
# Al elegir la opción 1 el usuario podrá ingresar la frase que quiera    
    if opcion == "1":
        palabra = input("\nIngresa una palabra: ")
        longitud = len(palabra)
 #El programa podra leer la loongitud de la frase.       
        if 4 <= longitud <= 8:
            print("La palabra es correcta.")
# Si la frase es menor de 4 letras el programa le comentara que le hace faltas letras.
        elif longitud < 4:
            print(f"Hacen falta letras. Solo tiene {longitud} letra{'s' if longitud != 1 else ''}.")
# si la frase contiene más de 8 letras el programa le determinara que excede de la cantidad requerida.
        else:
            print(f"Sobran letras. Tiene {longitud} letras.")
        
        # Mostrar cada letra usando for
        print("Letras de la palabra:", end=" ")
        for letra in palabra:
            print(letra, end=" ")
        print()
# Al elegir la opción 2 el sistema concluye    
    elif opcion == "2":
        print("¡Hasta luego!")
        break
    
    else:
        print("Opción no válida. Por favor ingrese 1 o 2.")

###########################################################
####################### Plano carteciano ############### El usuaro podra ingresar los datos requeridos ede un plano carteciono el cual le indicara en que cuadrante se encuentra.
def encontrar_cuadrante():
    while True:
        try:
            x = float(input("Ingrese la coordenada X: "))
            y = float(input("Ingrese la coordenada Y: "))

            if x == 0 and y == 0:
                print("El punto está en el origen (0,0)")
            elif x == 0:
                print(f"El punto ({x}, {y}) está sobre el eje Y")
            elif y == 0:
                print(f"El punto ({x}, {y}) está sobre el eje X")
#el sistema tiene la oportunidad indicar en cue cuadrante esta en positivos o negativos.
            elif x > 0 and y > 0:
                print(f"El punto ({x}, {y}) se encuentra en el Cuadrante I")
            elif x < 0 and y > 0:
                print(f"El punto ({x}, {y}) se encuentra en el Cuadrante II")
            elif x < 0 and y < 0:
                print(f"El punto ({x}, {y}) se encuentra en el Cuadrante III")
            elif x > 0 and y < 0:
                print(f"El punto ({x}, {y}) se encuentra en el Cuadrante IV")
#al tener el valor requerido concluira el programa, si elusuario desea continuar podra elegir entre la opción 1 o 2 para concluir.
            while True:
                continuar = input("\n¿Deseas continuar (1) o Terminar (2): ")
                if continuar == "1":
                    print("\nIngresa las nuevas coordenadas")
                    break  
                elif continuar == "2":
                    print("\n¡Gracias por usar el identificador de cuadrantes!")
                    return  
                else:
                    print("Opción no válida. Por favor ingrese 1 para continuar o 2 para terminar")

        except ValueError:
            print("Error: Por favor ingrese valores numéricos válidos.\n")

if __name__ == "__main__":
    print("Identificador de cuadrantes en el plano cartesiano")
    print("-----------------------------------------------\n")
    encontrar_cuadrante()
