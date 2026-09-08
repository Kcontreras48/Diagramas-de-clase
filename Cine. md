classDiagram
    class Usuario {
        +int id
        +String nombre
        +String email
        +String contrasena
        +iniciarSesion()
        +registrarse()
    }

    class Cliente {
        +String telefono
        +consultarHistorial()
    }

    class Pelicula {
        +int id
        +String titulo
        +String sinopsis
        +int duracionMinutos
        +String clasificacion
        +String genero
    }

    class Sala {
        +int id
        +int numero
        +int capacidad
        +String tipoScreen
    }

    class Asiento {
        +int id
        +String fila
        +int numero
        +String estado
        +bloquear()
        +liberar()
    }

    class Funcion {
        +int id
        +DateTime fechaHora
        +float precioBase
        +obtenerAsientosDisponibles()
    }

    class Reserva {
        +int id
        +DateTime fechaCreacion
        +String estado
        +float total
        +calcularTotal()
        +cancelar()
    }

    class Boleta {
        +int id
        +String codigoQR
        +float precio
        +generarQR()
    }

    class Pago {
        +int id
        +float monto
        +DateTime fecha
        +String metodoPago
        +String estado
        +procesarPago()
    }

    Usuario <|-- Cliente
    Pelicula "1" -- "0..*" Funcion : tiene
    Sala "1" -- "0..*" Funcion : alberga
    Sala "1" *-- "1..*" Asiento : contiene
    Cliente "1" -- "0..*" Reserva : realiza
    Funcion "1" -- "0..*" Reserva : pertenece a
    Reserva "1" *-- "1..*" Boleta : contiene
    Asiento "1" -- "0..*" Boleta : asignado a
    Reserva "1" -- "1" Pago : se liquida con
