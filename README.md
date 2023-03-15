
# Dogs
See the characteristics of your dog

En python

# Definir un diccionario con los datos de algunas razas de perros
perros = {
    "Labrador Retriever": {
        "min_life_expectancy": 10,
        "max_life_expectancy": 12,
        "max_height_male": 62,
        "max_height_female": 57,
        "max_weight_male": 36,
        "max_weight_female": 32,
        "min_height_male": 57,
        "min_height_female": 55,
        "min_weight_male": 27,
        "min_weight_female": 25,
        "good_with_children": True,
        "good_with_other_dogs": True,
        "shedding": True,
        "grooming": 2,
        "drooling": False,
        "coat_length": "short",
        "good_with_strangers": 3,
        "playfulness": 5,
        "protectiveness": 3,
        "trainability": 5,
        "energy": 5,
        "barking": 2
    },
    "Golden Retriever": {
        "min_life_expectancy": 10,
        "max_life_expectancy": 12,
        "max_height_male": 61,
        "max_height_female": 56,
        "max_weight_male": 34,
        "max_weight_female": 32,
        "min_height_male": 56,
        "min_height_female": 55,
        "min_weight_male": 27,
        "min_weight_female": 25,
        "good_with_children": True,
        "good_with_other_dogs": True,
        "shedding": True,
        "grooming": 2,
        "drooling": False,
        "coat_length": "long",
        "good_with_strangers": 3,
        "playfulness": 5,
        "protectiveness": 3,
        "trainability": 5,
        "energy": 5,
        "barking": 2
    },
    "Bulldog": {
        "min_life_expectancy": 8,
        "max_life_expectancy": 10,
        "max_height_male": 40,
        "max_height_female": 40,
        "max_weight_male": 25,
        "max_weight_female": 23,
        "min_height_male": 36,
        "min_height_female": 36,
        "min_weight_male": 22,
        "min_weight_female": 19,
        "good_with_children": 3,
        "good_with_other_dogs": 2,
        "shedding": True,
        "grooming": 1,
        "drooling": True,
        "coat_length": "short",
        "good_with_strangers": 1,
        "playfulness": 3,
        "protectiveness": 5,
        "trainability": 2,
        "energy": 2,
        "barking": 2
    }
}

# Crear un menú que permita al usuario seleccionar una raza y mostrar sus características
while True:
    print("Seleccione una raza de perro:")
    for index


____________________________________________________

import pandas as pd

# Leer los datos de la tabla en un DataFrame de Pandas
datos = pd.read_csv("tabla_perros.csv")

# Crear un diccionario para almacenar los datos de cada raza de perro
perros = {}

# Iterar sobre las filas del DataFrame y agregar los datos de cada raza al diccionario
for i, fila in datos.iterrows():
    raza = fila["Name"]
    datos_raza = {
        "min_life_expectancy": fila["min_life_expectancy"],
        "max_life_expectancy": fila["max_life_expectancy"],
        "max_height_male": fila["max_height_male"],
        "max_height_female": fila["max_height_female"],
        "max_weight_male": fila["max_weight_male"],
        "max_weight_female": fila["max_weight_female"],
        "min_height_male": fila["min_height_male"],
        "min_height_female": fila["min_height_female"],
        "min_weight_male": fila["min_weight_male"],
        "min_weight_female": fila["min_weight_female"],
        "good_with_children": fila["good_with_children"],
        "good_with_other_dogs": fila["good_with_other_dogs"],
        "shedding": fila["shedding"],
        "grooming": fila["grooming"],
        "drooling": fila["drooling"],
        "coat_length": fila["coat_length"],
        "good_with_strangers": fila["good_with_strangers"],
        "playfulness": fila["playfulness"],
        "protectiveness": fila["protectiveness"],
        "trainability": fila["trainability"],
        "energy": fila["energy"],
        "barking": fila["barking"]
    }
    perros[raza] = datos_raza

# Mostrar el diccionario resultante
print(perros)
