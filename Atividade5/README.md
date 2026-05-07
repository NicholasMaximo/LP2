# pAtividadeFive

Projeto Windows Forms em C# (.NET Framework 4.8) com 4 exercícios de manipulação de strings e cálculos.

---

## Exercício 1 — Manipulação de Texto (`frmExercicio1`)

Formulário com um `RichTextBox` e três botões:

### Botão: Quantidade de Espaços em Branco
Percorre o texto com `for` e conta todos os espaços em branco usando `char.IsWhiteSpace`. Exibe a posição do primeiro espaço encontrado e a quantidade total.

### Botão: Número de vezes que a letra R aparece
Percorre o texto com `foreach` e conta quantas vezes a letra `R` (maiúscula ou minúscula) aparece.

### Botão: Número de Pares de Letras
Percorre o texto com `while` e conta pares de letras iguais e adjacentes (ex: "ss" em "pessoas"). A cada par encontrado, avança 2 posições para não recontar o mesmo par.

---

## Exercício 2 — Número H (`frmExercicio2`)

Calcula o número H a partir de um valor N fornecido pelo usuário:

```
H = 1 + 1/2 + 1/3 + ... + 1/N
```

- Valida se N é um inteiro maior que 0
- Usa `for` para acumular a soma
- Exibe o resultado com 2 casas decimais

---

## Exercício 3 — Palíndromo (`frmExercicio3`)

Verifica se uma sequência de caracteres é um palíndromo (leitura igual da esquerda para a direita e vice-versa).

- Limita a entrada a no máximo 50 caracteres
- Converte o texto para maiúsculo
- Remove espaços em branco se houver
- Compara os caracteres das extremidades para o centro com `for`
- Exibe o resultado em um segundo TextBox

Exemplos válidos: `OSSO`, `OVO`, `SUBI NO ONIBUS`

---

## Exercício 4 — Cálculo de Salário Bruto (`frmExercicio4`)

Calcula o salário bruto de um funcionário com base na fórmula:

```
Salário Bruto = A + A × (0,05×B + 0,1×C + 0,1×D) + Gratificação
```

Onde:
- `A` = Salário base
- `B` = 1 se Produção >= 100, senão 0
- `C` = 1 se Produção >= 120, senão 0
- `D` = 1 se Produção >= 150, senão 0

**Entradas:** Salário, Produção e Gratificação (validadas com `double.TryParse`)

**Restrição:** Salário bruto acima de R$ 7.000,00 só é permitido para funcionários com Produção >= 150 **e** com gratificação. Caso contrário, o salário é limitado a R$ 7.000,00 e uma mensagem é exibida.

---

## Estrutura do Projeto

```
pAtividadeFive/
├── Form1.cs                  # Formulário principal (menu de navegação)
├── frmExercicio1.cs          # Exercício 1 - Manipulação de texto
├── frmExercicio2.cs          # Exercício 2 - Número H
├── frmExercicio3.cs          # Exercício 3 - Palíndromo
├── frmExercicio4.cs          # Exercício 4 - Salário Bruto
├── Program.cs                # Ponto de entrada da aplicação
└── pAtividadeFive.csproj     # Arquivo de projeto
```

## Requisitos

- Visual Studio 2019 ou superior
- .NET Framework 4.8
