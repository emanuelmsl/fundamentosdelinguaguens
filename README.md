# 01 - Introdução às Linguagens de Programação

## Histórico

- **1957** – FORTRAN: Primeira linguagem de alto nível, focada em cálculos científicos.
- **1958** – LISP: Primeira linguagem funcional, usada em Inteligência Artificial.
- **1964** – BASIC: Desenvolvida para iniciantes.
- **1970** – Pascal: Linguagem estruturada para ensino.
- **1972** – C: Linguagem de sistemas influente.
- **1983** – C++: Extensão orientada a objetos do C.
- **1987** – Perl: Linguagem de script poderosa.
- **1991** – Python: Linguagem multiparadigma e de fácil leitura.
- **1995** – Java: Multiplataforma com máquina virtual (JVM).
- **1995** – JavaScript: Linguagem para web.
- **2000** – C#: Linguagem da Microsoft.
- **2009** – Go: Linguagem concorrente do Google.
- **2010** – Rust: Linguagem segura para sistemas.
- **2012** – TypeScript: JavaScript tipado.

## Objetivos

- Entender a evolução das linguagens.
- Reconhecer paradigmas e influências.

# 02 - Ambientes de Execução

## Tipos de Ambientes

- **Compilador**: Traduz o código-fonte diretamente para código de máquina.
- **Interpretador**: Executa o código-fonte linha a linha, sem gerar código de máquina.
- **Máquina Virtual**: Traduz o código-fonte para um código intermediário (bytecode), que é executado numa máquina virtual.

## Diagramas

## Exemplos

| Ambiente       | Linguagens Exemplares        |
|----------------|-----------------------------|
| Compilador     | C, Rust                     |
| Interpretador  | Python, Ruby                |
| Máquina Virtual| Java (JVM), C# (.NET CLR)   |

# 03 - Sintaxe e Semântica

## Mini-Gramática da Linguagem MiniLang
## Objetivos

- Entender como construir gramáticas formais.
- Diferenciar sintaxe (forma) e semântica (significado).

<br>

- # 04 - Tipos de Dados
## Comparativo entre Linguagens

### Python (tipagem dinâmica)

```python
x = "10" + 5  # Erro em tempo de execução
int x = "10" + 5; // Erro de compilação
let x = "10" + 5;  // Resultado: "105"

---

# 05-estruturas-de-controle/README.md

```markdown
# 05 - Estruturas de Controle

Estruturas que controlam o fluxo de execução do programa, como condicionais e laços.

## Exemplo em Python

```python
genero = input("Digite seu gênero favorito (acao/comedia/terror): ")
idade = int(input("Digite sua idade: "))

if genero == "acao":
    if idade >= 18:
        print("Recomendo: John Wick (2014)")
    else:
        print("Recomendo: Homem-Aranha (2002)")
elif genero == "comedia":
    print("Recomendo: Se Beber, Não Case (2009)")
else:
    print("Recomendo: O Iluminado (1980)")

for filme in ["Matrix", "Toy Story", "It"]:
    print(f"Já assistiu {filme}? (s/n)")
    resposta = input()
    if resposta == "s":
        print("Ótima escolha!")
        break

---

# 06-subprogramas/README.md

```markdown
# 06 - Subprogramas (Funções e Procedimentos)

## Passagem por Referência vs Valor

### Python (passagem por referência)

```python
def alterar_lista(lista):
    lista.append(42)
(c)
void soma(int a) {
    a = a + 10;
}

## Objetivos

- Visualizar a recursão e o funcionamento da pilha de execução.
- Compreender alocação e liberação de contexto de função.

# 08 - Programação Orientada a Objetos (POO)

## Exemplo em Python

```python
class Personagem:
    def __init__(self, nome):
        self.nome = nome

    def falar(self):
        print(f"{self.nome} diz olá!")

class Guerreiro(Personagem):
    def atacar(self):
        print(f"{self.nome} ataca com espada!")

---

# 09-concorrencia/README.md

```markdown
# 09 - Concorrência

## Threads e Processos

- **Thread**: Unidade de execução dentro do mesmo processo (memória compartilhada).
- **Processo**: Instância independente do programa (memória isolada).

## Exemplo em Python

```python
import threading

def contador(inicio, fim):
    for i in range(inicio, fim):
        print(i)

# Duas threads no mesmo processo
t1 = threading.Thread(target=contador, args=(1, 5))
t2 = threading.Thread(target=contador, args=(11, 15))
t1.start()
t2.start()

---

# 10-gerenciamento-memoria/README.md

```markdown
# 10 - Gerenciamento de Memória

| Aspecto           | Java                             | C                       |
|-------------------|---------------------------------|-------------------------|
| Alocação          | Automática (new)                 | Manual (malloc)          |
| Liberação         | Garbage Collector               | Manual (free)            |
| Segurança         | Verificação de limites           | Acesso direto            |
| Performance       | Overhead do GC                   | Controle total           |

## Objetivos

- Comparar gerenciamento manual vs automático.
- Entender vantagens e desvantagens.
# 11 - Programação Funcional

## Exemplos em Python

```python
from functools import reduce

# Fatorial com recursão e reduce
fatorial = lambda n: 1 if n == 0 else reduce(lambda x, y: x*y, range(1, n+1))

# Filtrar números pares e dobrá-los
numeros = [1, 2, 3, 4, 5]
resultado = list(map(lambda x: x*2, filter(lambda x: x%2 == 0, numeros)))
# [4, 8]
---
# 12-programacao-logica/README.md

```markdown
# 12 - Programação Lógica

## Exemplo em Prolog

```prolog
pai(joao, maria).
pai(joao, pedro).
mae(ana, maria).
mae(ana, pedro).

irmao(X, Y) :- pai(P, X), pai(P, Y), mae(M, X), mae(M, Y), X \= Y.

---

# 13-scripts-web/README.md

```markdown
# 13 - Scripts para Web e Automação

## Script para organizar arquivos por extensão

```python
import os
import shutil

def organizar_diretorio(diretorio):
    for arquivo in os.listdir(diretorio):
        if os.path.isfile(os.path.join(diretorio, arquivo)):
            ext = arquivo.split('.')[-1]
            pasta_ext = os.path.join(diretorio, ext)

            if not os.path.exists(pasta_ext):
                os.mkdir(pasta_ext)

            shutil.move(
                os.path.join(diretorio, arquivo),
                os.path.join(pasta_ext, arquivo)
            )

organizar_diretorio('./downloads')

---

# 14-tendencias/README.md

```markdown
# 14 - Tendências em Linguagens de Programação

## Rust

- Linguagem de sistemas com performance comparável a C/C++.
- Segurança de memória sem garbage collector.
- Concorrência sem data races.
- Sistema de ownership inovador.

## Exemplo

```rust
fn main() {
    let mut s = String::from("hello");
    s.push_str(", world!");
    println!("{}", s); // hello, world!
    
    // Ownership previne referências inválidas
    let s1 = String::from("Rust");
    let s2 = s1; // s1 é movido para s2
    // println!("{}", s1); // Erro! s1 não é mais válido
}

---

---






