import random

def inicializar_notas(num_estudiantes, num_materias):
    notas = []
    for _ in range(num_estudiantes):
        fila_notas = [random.randint(0, 100) for _ in range(num_materias)]
        notas.append(fila_notas)
    return notas

def calcular_promedios(notas):
    promedios = [sum(estudiante) / len(estudiante) for estudiante in notas]
    return promedios

def ordenar_notas(notas):
    for estudiante in notas:
        estudiante.sort(reverse=True)

def buscar_nota_extrema(notas, materia, extrema):
    if extrema == "max":
        return max(estudiante[materia] for estudiante in notas)
    elif extrema == "min":
        return min(estudiante[materia] for estudiante in notas)

def imprimir_notas_promedios_extremas(notas, promedios, materia):
    print("Notas de los estudiantes:")
    for estudiante in notas:
        print(estudiante)
    print("Promedios de notas de los estudiantes:", promedios)
    print(f"Nota más alta en la materia {materia+1}: {buscar_nota_extrema(notas, materia, 'max')}")
    print(f"Nota más baja en la materia {materia+1}: {buscar_nota_extrema(notas, materia, 'min')}")

num_estudiantes = 5
num_materias = 3

notas = inicializar_notas(num_estudiantes, num_materias)
promedios = calcular_promedios(notas)
ordenar_notas(notas)

materia_especifica = 0  # Cambiar a la materia específica que desees
imprimir_notas_promedios_extremas(notas, promedios, materia_especifica)
