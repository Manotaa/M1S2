
inventario = []

def agregar_producto():
    """Register a new product with validation"""

    print("\n--- ADD PRODUCT ---")

    nombre = input("Enter product name: ").strip()

    
    while True:
        try:
            precio = float(input("Enter product price: "))
            if precio < 0:
                print("Price cannot be negative.")
            else:
                break
        except ValueError:
            print("Invalid input. Enter a valid number.")

    
    while True:
        try:
            cantidad = int(input("Enter product quantity: "))
            if cantidad < 0:
                print("Quantity cannot be negative.")
            else:
                break
        except ValueError:
            print("Invalid input. Enter a valid integer.")

   
    producto = {
        "nombre": nombre,
        "precio": precio,
        "cantidad": cantidad
    }

    
    inventario.append(producto)

    print("Product added successfully.")



def mostrar_inventario():
    """Display all products"""

    print("\n--- INVENTORY ---")

    if len(inventario) == 0:
        print("Inventory is empty.")
        return

    for producto in inventario:
        print(f"Product: {producto['nombre']} | Price: {producto['precio']} | Quantity: {producto['cantidad']}")



def calcular_estadisticas():
    """Calculate total value and total products"""

    print("\n--- INVENTORY STATISTICS ---")

    if len(inventario) == 0:
        print("Inventory is empty.")
        return

    total_valor = 0
    total_productos = 0

    for producto in inventario:
        total_valor += producto["precio"] * producto["cantidad"]
        total_productos += producto["cantidad"]

    print(f"Total inventory value: {total_valor}")
    print(f"Total number of products: {total_productos}")


def mostrar_menu():
    print("\n===== INVENTORY MENU =====")
    print("1. Add product")
    print("2. Show inventory")
    print("3. Calculate statistics")
    print("4. Exit")



def main():
    opcion = ""

    while opcion != "4":
        mostrar_menu()
        opcion = input("Choose an option: ").strip()

        if opcion == "1":
            agregar_producto()
        elif opcion == "2":
            mostrar_inventario()
        elif opcion == "3":
            calcular_estadisticas()
        elif opcion == "4":
            print("Goodbye.")
        else:
            print("Invalid option. Try again.")


if __name__ == "__main__":
    main()
