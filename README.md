#  Sistema de Gestion de Torneos Deportivos

##  Descripción del Sistema
Este sistema modela la gestión de competencias deportivas, incluyendo ligas y torneos de eliminación, equipos, jugadores, partidos y resultados.

##  Integrantes
Juan Esteban Muñoz Vargas | jemunoz-2025a@corhuila.edu.co |
Santiago Marin Franco | samarin-2025a@corhuila.edu.co |

##  Diagrama de Clases UML
Clase Competencia (Abstracta)

Atributos:

id: int
nombre: String
fechaInicio: Date
fechaFin: Date
tipo: String
estado: String
numeroEquipos: int
premio: double
organizador: String

Métodos:

agregarEquipo(equipo: Equipo): void
generarFixture(): void
calcularTabla(): void
 TorneoLiga (Hereda de Competencia)

Atributos:

jornadas: int
puntosPorVictoria: int
puntosPorEmpate: int

Métodos:

generarFixture(): void
calcularTabla(): void
 TorneoEliminacion (Hereda de Competencia)

Atributos:

rondas: int
equiposClasificados: int

Métodos:

generarFixture(): void
calcularTabla(): void
 TablaPosiciones

Atributos:

golesLocal: int
puntos: int
partidosJugados: int
victorias: int
derrotas: int
empates: int

Métodos:

actualizarPuntos(): void
calcularPosicion(): void
mostrarTabla(): void
 Equipo

Atributos:

idEquipo: int
nombre: String
ciudad: String
entrenador: String

Métodos:

agregarJugador(jugador: Jugador): void
 Jugador

Atributos:

idJugador: int
nombre: String
edad: int
posicion: String
numero: int
nacionalidad: String
 Partido

Atributos:

idPartido: int
fecha: Date
equipoLocal: Equipo
equipoVisitante: Equipo

Métodos:

jugar(): void
 Interfaz Jugable

Métodos:

jugar(): void
calcularResultado(): void
 Resultado

Atributos:

golesLocal: int
golesVisitante: int
estado: String (jugado, pendiente)


