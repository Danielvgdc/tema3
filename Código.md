``` mermaid

classDiagram
    class Libro {
        - nombre: String
        - tipo: String
        - editorial: String
        - año: int
        - autores: String
    }

    class Ejemplar {
        - id: int
        - estado: String
        - Libro:
    }

    class Autor {
        - nombre: String
        - nacionalidad: String
        - fechaNac: String
    }

    class Lector {
        - DNI: String
        - numeroSocio: int
        - nombre: String
        - direción: String
    }

    Libro "1" --* "N" Ejemplar
    Ejemplar "N" *-- "1" Autor
    Autor "1" --* "N" Lector
