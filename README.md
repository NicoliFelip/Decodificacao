# Decodificacao

import hashlib
import itertools
import string

# Parte fixa do link
base = "https://forms.layers.education/4rrzwnl5sv{}n3yuu6ee8?answ=636cbe9"
target_hash = "df155cdc10d7a2ed691f2e0e094ee287"

# Gera todas as combinações possíveis de 2 caracteres (letras e números)
chars = string.ascii_letters + string.digits  # abc...XYZ0123...
for combo in itertools.product(chars, repeat=2):
    attempt = base.format("".join(combo))
    result_hash = hashlib.md5(attempt.encode()).hexdigest()
    if result_hash == target_hash:
        print(f"Match encontrado: {attempt}")
        break
