# Definir la isla
isla = {
    "playa": {
        "descripcion": "Estás en la playa de la isla.",
        "norte": "jungla",
        "sur": "pantano",
        "este": "montaña",
        "oeste": "cueva"
    },
    "jungla": {
        "descripcion": "Estás en la jungla.",
        "norte": "río",
        "sur": "playa",
        "este": "montaña",
        "oeste": "pantano"
    },
    "pantano": {
        "descripcion": "Estás en el pantano.",
        "norte": "jungla",
        "sur": "cueva",
        "este": "playa",
        "oeste": "montaña"
    },
    "montaña": {
        "descripcion": "Estás en la montaña.",
        "norte": "cima",
        "sur": "jungla",
        "este": "pantano",
        "oeste": "playa"
    },
    "cueva": {
        "descripcion": "Estás en la cueva.",
        "norte": "pantano",
        "sur": "playa",
        "este": "jungla",
        "oeste": "montaña"
    },
    "río": {
        "descripcion": "Estás en el río.",
        "norte": "cima",
        "sur": "jungla",
        "este": "montaña",
        "oeste": "pantano"
    },
    "cima": {
        "descripcion": "Estás en la cima de la montaña.",
        "tesoro": True
    }
}

# Definir el jugador
jugador = {
    "ubicacion": "playa",
    "vidas": 5
}

# Función para mover al jugador
def mover(direccion):
    global jugador
    if direccion in isla[jugador["ubicacion"]]:
        jugador["ubicacion"] = isla[jugador["ubicacion"]][direccion]
    else:
        print("No puedes ir en esa dirección.")

# Función para interactuar con objetos y personajes
def interactuar():
    global jugador
    print(isla[jugador["ubicacion"]]["descripcion"])
    if "tesoro" in isla[jugador["ubicacion"]]:
        print("¡Has encontrado el tesoro!")
        return False
    return True

# Juego principal
while True:
    print("Ubicación:", jugador["ubicacion"])
    print("Vidas:", jugador["vidas"])
    accion = input("¿Qué deseas hacer? (mover, interactuar, salir): ")
    if accion == "mover":
        direccion = input("¿En qué dirección deseas moverte? (norte, sur, este, oeste): ")
        mover(direccion)
    elif accion == "interactuar":
        if not interactuar():
            break
    elif accion == "salir":
        break
    else:
        print("Acción inválida.")
    jugador["vidas"] -= 1
    if jugador["vidas"] <= 0:
        print("¡Has muerto! Game over.")
        break
