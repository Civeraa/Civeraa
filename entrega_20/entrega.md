#!/bin/bash



# Función para mostrar el menú

mostrar_menu() {

    echo "Menú:"

    echo "1. Crear carpeta"

    echo "2. Crear archivo"

    echo "3. Salir"

}



# Función para crear una carpeta

crear_carpeta() {

    echo "Ingrese el nombre de la carpeta:"

    read nombre_carpeta

    mkdir "$nombre_carpeta"

    echo "¡Carpeta creada con éxito!"

}



# Función para crear un archivo

crear_archivo() {
    echo "Ingrese el nombre del archivo:"

    read nombre_archivo

    touch "$nombre_archivo"

    echo "¡Archivo creado con éxito!"

}



# Bucle principal

while true; do

    mostrar_menu

    echo "Ingrese su elección:"

    read opcion



    case $opcion in

        1)

            crear_carpeta

         
          ;;
        2)

            crear_archivo

            ;;

        3)

            echo "Saliendo del programa."

            break

            ;;

        *)

            echo "Opción no válida. Por favor, seleccione una opción válida."

            ;;

    esac

done



