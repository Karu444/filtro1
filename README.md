import json

# Función para guardar los datos en un archivo JSON


def guardar_datos_en_json(datos, nombre_archivo):
    with open(nombre_archivo, 'w') as archivo:
        json.dump(datos, archivo)

# Función para cargar los datos desde un archivo JSON


def cargar_datos_desde_json(nombre_archivo):
    try:
        with open(nombre_archivo, 'r') as archivo:
            return json.load(archivo)
    except FileNotFoundError:
        return {}


# Crear o cargar el archivo JSON para los registros del día
nombre_archivo_registros = 'registros.json'
registros_diarios = cargar_datos_desde_json(nombre_archivo_registros)

 #    def clientes ():
  #       "ids" :  [],
   #      "noms" : [],
    #     "ccs" :  [],
     #    "nums" : [],
      #   "cels" : [],
  

def leerInt(msg):
    while True:
        try:
            print("_" * 75)
            iNum = int(input(msg))
            return iNum
        except ValueError:
            print("_" * 75)
            print("Ingrese un numero entero valido")


def leerString(msg):
    while True:
        try:
            sNom = input(msg)
            if sNom.strip() == "":
                print("\nPor favor ingrese un nombre valido")
                continue
            return sNom
        except Exception as e:
            print("\nError al ingresar un nombre", e.message)


# Función para agregar un cliente
def agregar_cliente():

    idcliente = input("<<< Ingrese el ID del cliente >>>: ")
    if idcliente == "":
        print("XXX |ERROR|. ¡No pueden haber espacios en blanco!. XXXX")
        print("        / \  w  / \ ")
        print("    \ \   >     <  / /")
        print("    =    0  >º<  0   =")
        print("       =          = ")
        print("           ===         ==7")
        print("          (  v  )     //")
        print("         (  vvv  ) ==//  ")
        print("         \  / \  /")
        print("      ^  nnn   nnn  ^")
        print("   ^^^^^^^^^^^^^^^^^^^  ")
        return
    cedula = input("<<< Ingrese el número de cédula del cliente >>>: ")
    if cedula == "":
        print("XXX |ERROR|. ¡No pueden haber espacios en blanco!. XXXX")
        print("        / \  w  / \ ")
        print("    \ \   >     <  / /")
        print("    =    0  >º<  0   =")
        print("       =          = ")
        print("           ===         ==7")
        print("          (  v  )     //")
        print("         (  vvv  ) ==//  ")
        print("         \  / \  /")
        print("      ^  nnn   nnn  ^")
        print("   ^^^^^^^^^^^^^^^^^^^  ")
        return
    nombre = input("<<< Ingrese el nombre del cliente >>>: ")
    if nombre == "":
        print("XXX |ERROR|. ¡No pueden haber espacios en blanco!. XXXX")
        print("        / \  w  / \ ")
        print("    \ \   >     <  / /")
        print("    =    0  >º<  0   =")
        print("       =          = ")
        print("           ===         ==7")
        print("          (  v  )     //")
        print("         (  vvv  ) ==//  ")
        print("         \  / \  /")
        print("      ^  nnn   nnn  ^")
        print("   ^^^^^^^^^^^^^^^^^^^  ")
        return
    if nombre == "1" or "2" or "3" or "4" or "5" or "6" or "7" or "8" or "9" or "0":
        print("XXXX |ERROR|. No pueden haber numeros en el nombre. XXXX")
        print("        / \  w  / \ ")
        print("    \ \   >     <  / /")
        print("    =    0  >º<  0   =")
        print("       =          = ")
        print("           ===         ==7")
        print("          (  v  )     //")
        print("         (  vvv  ) ==//  ")
        print("         \  / \  /")
        print("      ^  nnn   nnn  ^")
        print("   ^^^^^^^^^^^^^^^^^^^  ")
        return
    celular = input("<<< ingrese el numero de celular del cliente >>>: ")
    if celular == "":
        print("XXX |ERROR|. ¡No pueden haber espacios en blanco!. XXXX")
        print("        / \  w  / \ ")
        print("    \ \   >     <  / /")
        print("    =    0  >º<  0   =")
        print("       =          = ")
        print("           ===         ==7")
        print("          (  v  )     //")
        print("         (  vvv  ) ==//  ")
        print("         \  / \  /")
        print("      ^  nnn   nnn  ^")
        print("   ^^^^^^^^^^^^^^^^^^^  ")
        return
    sexo = input("<<< ingrese el sexo del cliente (M/F) >>>: ")
    if sexo == "":
        print("XXX |ERROR|. ¡No pueden haber espacios en blanco!. XXXX")
        print("        / \  w  / \ ")
        print("    \ \   >     <  / /")
        print("    =    0  >º<  0   =")
        print("       =          = ")
        print("           ===         ==7")
        print("          (  v  )     //")
        print("         (  vvv  ) ==//  ")
        print("         \  / \  /")
        print("      ^  nnn   nnn  ^")
        print("   ^^^^^^^^^^^^^^^^^^^  ")
        return
    elif sexo != "M" or "F":
        print("xxxx |ERROR|. Sexo erroneo xxxxx")
        print("        / \  w  / \ ")
        print("    \ \   >     <  / /")
        print("    =    0  >º<  0   =")
        print("       =          = ")
        print("           ===         ==7")
        print("          (  v  )     //")
        print("         (  vvv  ) ==//  ")
        print("         \  / \  /")
        print("      ^  nnn   nnn  ^")
        print("   ^^^^^^^^^^^^^^^^^^^  ")
        return
    clientes[idcliente] = nombre
    print("*** Cliente agregado exitosamente.***")
    print("        / \  w  / \ ")
    print("    \ \   >     <  / /")
    print("    =    n  >º<  n   =")
    print("       =          = ")
    print("           ===         ==7")
    print("          (  v  )     //")
    print("         (  vvv  ) ==//  ")
    print("         \  / \  /")
    print("      ^  nnn   nnn  ^")
    print("   ^^^^^^^^^^^^^^^^^^^  ")

    

# Función para agregar una tarjeta


def agregar_tarjeta():
    verificod = input("<<<Ingrese el codigo de verificacion (100/999)>>>: ")
    if verificod == "":
        
        print("XXXX |ERROR|. No pueden haber espacios en blanco. XXXX")
        return
    elif verificod >999 or verificod <100:
        print("XXXX codigo invalido. debe estar en el rango de 100 y 999 XXXX")
        return
    codigo = input("<<<Ingrese el código del banco>>>: ")
    if codigo == "":
        print("XXX |ERROR|. ¡No pueden haber espacios en blanco!. XXXX")
        print("        / \  w  / \ ")
        print("    \ \   >     <  / /")
        print("    =    0  >º<  0   =")
        print("       =          = ")
        print("           ===         ==7")
        print("          (  v  )     //")
        print("         (  vvv  ) ==//  ")
        print("         \  / \  /")
        print("      ^  nnn   nnn  ^")
        print("   ^^^^^^^^^^^^^^^^^^^  ")
        return
    tipodetarj = input("Ingrese el tipo de la tarjeta de credito: ")
    if tipodetarj == "":
        print("XXX |ERROR|. ¡No pueden haber espacios en blanco!. XXXX")
        print("        / \  w  / \ ")
        print("    \ \   >     <  / /")
        print("    =    0  >º<  0   =")
        print("       =          = ")
        print("           ===         ==7")
        print("          (  v  )     //")
        print("         (  vvv  ) ==//  ")
        print("         \  / \  /")
        print("      ^  nnn   nnn  ^")
        print("   ^^^^^^^^^^^^^^^^^^^  ")
        return
    numerotarj = input("Ingrese el numero de tarjeta de credito del cliente: ")
    if numerotarj == "":
        print("XXX |ERROR|. ¡No pueden haber espacios en blanco!. XXXX")
        print("        / \  w  / \ ")
        print("    \ \   >     <  / /")
        print("    =    0  >º<  0   =")
        print("       =          = ")
        print("           ===         ==7")
        print("          (  v  )     //")
        print("         (  vvv  ) ==//  ")
        print("         \  / \  /")
        print("      ^  nnn   nnn  ^")
        print("   ^^^^^^^^^^^^^^^^^^^  ")
        return
    validez = input("Ingrese el tiempo de validez: ")
    if validez == "":
        print("XXX |ERROR|. ¡No pueden haber espacios en blanco!. XXXX")
        print("        / \  w  / \ ")
        print("    \ \   >     <  / /")
        print("    =    0  >º<  0   =")
        print("       =          = ")
        print("           ===         ==7")
        print("          (  v  )     //")
        print("         (  vvv  ) ==//  ")
        print("         \  / \  /")
        print("      ^  nnn   nnn  ^")
        print("   ^^^^^^^^^^^^^^^^^^^  ")
        return

    clientes[verificod] = numerotarj
    print("tarjeta agregada exitosamente.")


def vinvularclientetarj():
    ide = input("Ingrese el codigo del cliente: ")
    if ide not in clientes:
        print("Cliente no registrado.")
        return

    datosganerales = []

    while True:
        verificod = input(
            "Ingrese el código de verificacion de la tarjeta de credito: ")

        if verificod not in verificod:
            print("tarjeta no registrada.")
            continue

        agregar_cliente.append({
            "id": ["idcliente"],
            "cedula": ["cedula"]
        })

        print(
            f"La tarjeta [verificod] de tipo [tipotarj] queda a nombre de [nombre] de cedula [cedula] codigo [idcliente]")

def modificar():
    try:
        id = leerInt("Ingrese el id del empleado: ")
        e = ids.index(id)
    except ValueError:
        print("El empleando no existe.")
        input("Presione cualqueir tecla para volver al menu...")
        return

    print("\nMENU DE MODIFICACION")
    print("\n1. Nombre")
    print("\n2. Cedula")
    print("\n3. Numero")
    print("\n4. Sexo")

    while True:
        op = leerInt("Seleccione el que quiere modificar: ")
        if op < 1 or op > 4:
            print("Ingrese un valor valido")
            continue
        break
    if op == 1:
        print("Modificar nombre")
        nueNom = leerString("Ingrese el nuevo nombre: ")
        # noms.insert(e, nueNom)
        nombre[e] = nueNom
    elif op == 2:
        print("Modificar cedula")
        while True:
            nueHor = leerInt(
                "Ingrese el nuevo numero de cedula del cliente: ")
           
    elif op == 3:
        print("Modificar numero celular")
        while True:
            nueValor = leerInt("Ingrese el nuvo numero celular: ")
def buscar():
    id = leerInt("Ingrese el id del empleado: ")
    e = ids.index(id)
    
def cargar_datos():
    clientes = []
    if os.path.isfile("crediacme.json"):
        with open("crediacme.json", "r") as archivo:
            lineas = archivo.readlines()
            encabezados = lineas[0].strip().split(";")
            for linea in lineas[1:]:
                datos = linea.strip().split(";")
                empleado = dict(zip(encabezados, datos))
                clientes.append(empleado)
    return clientes
def guardar_datos(clientess):
    with open("distriacme.json", "w") as archivo:
        if clientes:
            encabezados = ";".join(clientess[0].keys())
            archivo.write(tarjetas + "\n")
            datos_linea = ";".join(datos)
            archivo.write(datos_linea + "\n")


# if clientes not in idcliente:
#            print("cliente no registrado.")
#           continue
# Menú principal del programa
clientes = {}
tarjetas = {}

while True:
    print("\n================ CREDITO ACME ===============")
    print("/*" *22 + "/")
    print("=" * 45)
    print("")
    print("1. ***        | Agregar cliente. |        ***")
    print("2. ***        | Agregar tarjeta. |        ***")
    print("3. *** |vincular tarjeta con el cliente.| ***")
    print("4. ***        |modificar cliente.|        ***")
    print("5. ***        | buscar cliente.  |        ***")
    print("0.            | >>>> Salir. <<<< |")
    print("")
    print("=" * 45)
    print("/*" *22 + "/")
    opcion = input(">>>> Seleccione una opción >>>> (0/1/2/3/4/5): ")

    if opcion == '1':
        agregar_cliente()
    elif opcion == '2':
        agregar_tarjeta()
    elif opcion == '3':
        vinvularclientetarj()
    elif opcion == '4':
        modificar()
    elif opcion == '5':
        buscar()
    elif opcion == '0':
        # Guardar los datos en el archivo JSON
        guardar_datos_en_json(registros_diarios, nombre_archivo_registros)
        print("Gracias por usar el programa. Registros diarios guardados.")
        break
    else:
        print("Opción inválida. Por favor, seleccione una opción válida (1/2/3/4).")


