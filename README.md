# Mi-primer-programa
Mi primer programa en Python
[TIENDA PYTHON.py](https://github.com/user-attachments/files/29612846/TIENDA.PYTHON.py)
def mostrar_modelos_camisetas(prenda):
    print(f"Has seleccionado {prenda}.")
    print("Escoge cuál de los dos modelos deseas:")
    print("1. Camiseta Oversize..........20.00$")
    print("2. Camiseta Boxy Fit..........22.00$")
    opcion = input("Selecciona el número del modelo (1 o 2): ")
    if opcion == "1":
        return 20.00
    elif opcion == "2":
        return 22.00
    else:
        print("Opción no válida. No se sumará nada al carrito.")
        return 0.0
def mostrar_modelos_pantalones(prenda):
    print(f"Has seleccionado {prenda}.")
    print("Escoge cuál de los dos modelos deseas:")
    print("1. Pantalón BAGGY.............35.00$")
    print("2. Pantalón skinny............25.00$")
    opcion = input("Selecciona el número del modelo (1 o 2): ")
    if opcion == "1":
        return 35.00
    elif opcion == "2":
        return 25.00
    else:
        print("Opción no válida. No se sumará nada al carrito.")
        return 0.0
def mostrar_modelos_chaquetas(prenda):
    print(f"Has seleccionado {prenda}.")
    print("Escoge cuál de los dos modelos deseas:")
    print("1. Chaqueta de Cuero..........40.00$")
    print("2. Chaqueta Jean..............38.00$")
    opcion = input("Selecciona el número del modelo (1 o 2): ")
    if opcion == "1":
        return 40.00
    elif opcion == "2":
        return 38.00
    else:
        print("Opción no válida. No se sumará nada al carrito.")
        return 0.0
def mostrar_modelos_zapatos(prenda):
    print(f"Has seleccionado {prenda}.")
    print("Escoge cuál de los dos modelos deseas:")
    print("1. zapatos Puma...............85.00$")
    print("2. Zapatos Nike...............75.00$")
    opcion = input("Selecciona el número del modelo (1 o 2): ")
    if opcion == "1":
        return 85.00
    elif opcion == "2":
        return 75.00
    else:
        print("Opción no válida. No se sumará nada al carrito.")
        return 0.0
def iniciar_tienda():
    print("--------------------------------------------------")
    print("------------BIENVENIDO A ELEGANSTER---------------")
    print("--------------------------------------------------")
    print("--HOY COMENZARÁS A VESTIR CON ESTILO--")
    nombre = input("Cuéntame cómo te llamas: ")
    print(f"Un gusto, {nombre}.")
    total_pago = 0.0
    continuar_comprando = "si"
    while continuar_comprando == "si":
        print("¿En cuáles de nuestras prendas estás interesado? (camisetas, pantalones, chaquetas, zapatos)")
        prenda = input("Escribe tu búsqueda: ").lower()
        print("--------------------------------------------------")
        cuenta_anterior = total_pago    
        if prenda == "camisetas":
            total_pago += mostrar_modelos_camisetas(prenda)
        elif prenda == "pantalones":
            total_pago += mostrar_modelos_pantalones(prenda)
        elif prenda == "chaquetas":
            total_pago += mostrar_modelos_chaquetas(prenda)
        elif prenda == "zapatos":
            total_pago += mostrar_modelos_zapatos(prenda)
        else:
            print(f"Lo siento, la prenda '{prenda}' no está disponible.")
        if total_pago > cuenta_anterior:
            print(f"¡Añadido al carrito! Subtotal actual: {total_pago}$")
        print("--------------------------------------------------")
        continuar_comprando = input("¿Deseas seguir buscando otra prenda? (si/no): ").lower()
    print("==================================================")
    print(f"GRACIAS POR COMPRAR EN ELEGANSTER, {nombre.upper()}.")
    print(f"EL TOTAL A PAGAR POR TU CUENTA ES: {total_pago}$")
    print("==================================================")
iniciar_tienda()
