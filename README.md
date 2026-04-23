# Decodificação - Desafio de Esteganografia — Maratona de Programação

Este projeto foi desenvolvido como parte de uma maratona de programação promovida pela startup Layers Education, em parceria com a IDWall.


# Contexto do Desafio

O desafio consistia em descobrir o complemento de uma URL parcialmente ocultada por uma técnica inspirada em esteganografia. Parte da informação estava mascarada e precisava ser reconstruída.

Além disso, foi fornecido um hash MD5 correspondente à URL correta, o que permitiu validar as tentativas geradas.


# Abordagem Utilizada

A solução utiliza um ataque de força bruta para testar todas as combinações possíveis de dois caracteres (letras maiúsculas, minúsculas e números) na parte desconhecida da URL.


# Para cada tentativa:

A combinação é inserida na URL base
O hash MD5 da URL completa é calculado
O resultado é comparado com o hash alvo
Quando há correspondência, a URL correta é encontrada

A biblioteca hashlib do Python é utilizada para gerar os hashes MD5 das tentativas.


# Tecnologias Utilizadas

Python
Biblioteca padrão hashlib
itertools para geração de combinações
Conceitos Envolvidos
Esteganografia (no contexto do desafio)
Hashing criptográfico (MD5)
Ataque de força bruta
Algoritmos e estruturas de dados


# Como Executar
Certifique-se de ter o Python instalado



Execute o script:

python nome_do_arquivo.py

O programa exibirá a URL correta quando encontrar o hash correspondente
