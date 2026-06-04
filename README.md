# SIMULADOR-DE-EXPEDICI-N-2D
Simulador en Python de una expedición en un mundo bidimensional. El usuario define parámetros iniciales como posición y energía. El programa simula movimientos por pasos con eventos aleatorios que afectan el recurso y la posición, y finaliza mostrando un informe con el resultado de la expedición.
import random
import random


# =====================================================
# FUNCIONES
# =====================================================

def pedir_numero(mensaje, minimo, maximo):

    while True:

        try:
            valor = int(input(mensaje))

            if minimo <= valor <= maximo:
                return valor

            else:
                print(f"Introduce un número entre {minimo} y {maximo}.")

        except ValueError:
            print("Debes escribir un número válido.")


def mostrar_estado(
    paso,
    x_antes,
    y_antes,
    x,
    y,
    energia_antes,
    energia,
    accion
):

    print("\n" + "=" * 50)
    print(f"PASO {paso}")
    print("=" * 50)

    print(f"Movimiento realizado: {accion}")

    print(f"Posición anterior: ({x_antes}, {y_antes})")
    print(f"Nueva posición: ({x
