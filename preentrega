productos = []
while True:
    print("\n" + "*"*30)
    print(f"{'GESTION DE PRODUCTOS':^30}")
    print("*"*30)
    print(f"{'Menú de Opciones':^30}")
    print("="*30)
    print("1. 💾 Ingresar Producto")
    print("2. 📄 Ver Productos Registrados")
    print("3. 🔎 Buscar Producto por Nombre")
    print("4. ❌ Eliminar Producto por Número")
    print("5. 🏃‍➡️ Salir")
    opcion = input("Seleccione una opción: ").strip()
    match opcion:   
        case "1":
            # Validación de entrada para el nombre y categoría
            while True:
                nombre = input("Nombre del producto: ").strip().title()
                if not nombre:
                    print("⚠️ El nombre es requerido. Intente nuevamente.")
                      
                else:
                    break    
            while True:
                categoria = input("Categoría: ").strip().title()
                if not categoria:
                    print("⚠️ La categoría es requerida. Intente nuevamente.")
                else:
                    break
            # Validación de entrada para el precio
            while True:
                precio = input("Precio (sin centavos): ").strip()
                if precio.isdigit():
                    precio = int(precio)
                    break
                else:
                    print("❌ El precio debe ser un número entero.")
            
            productos.append([nombre, categoria, precio])
            print("✅ Producto agregado exitosamente!")
        case "2":
            if not productos:
                print("⚠️ No hay productos registrados.")
            else:
                print("="*30)
                print(f"\n{'Lista de productos':^30}")
                print("="*30)
                for i in range(len(productos)):
                    print(f"{i +1}. Nombre: {productos[i][0]}, Categoría: {productos[i][1]}, Precio: ${productos[i][2]}")
        case "3":
            termino = input("Ingrese el nombre del producto a buscar: ").strip().lower()
            encontrados = []
            for prod in productos:
                if termino in prod[0].lower():
                    encontrados.append(prod)
                    
            if encontrados:
                print("="*30)
                print(f"\n{'Productos Encontrados':^30}")
                print("="*30)
                for prod in encontrados:
                    print(f"Nombre: {prod[0]}, Categoría: {prod[1]}, Precio: ${prod[2]}")
            else:
                print("⚠️ No se encontraron productos con ese nombre.")
        case "4":
            if not productos:
                print("⚠️ No hay productos registrados para eliminar!")
                continue
            else:
                print("="*30)
                print(f"\n{'Lista de productos':^30}")
                print("="*30)
                for i in range(len(productos)):
                    print(f"{i +1}. Nombre: {productos[i][0]}, Categoría: {productos[i][1]}, Precio: ${productos[i][2]}")           
            try:
                num = int(input("Ingrese el número del producto a eliminar: "))
                if 1 <= num <= len(productos):
                    eliminado = productos.pop(num-1)
                    print(f"✅ Producto '{eliminado[0]}' eliminado exitosamente!")
                else:
                    print("❌ Número inválido.")
            except ValueError:
                print("⚠️ Debe ingresar un número válido!")

        case "5":
            print("👋 Ha Salido del programa!")
            break
        case _:
            print("❌ Opción no válida. Intente nuevamente.")
