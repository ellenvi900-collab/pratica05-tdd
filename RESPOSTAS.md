### 1. No Ciclo 1 usamos `return 70`. Por que isso é aceitável no TDD? O que obrigou a escrever a soma de verdade?

No TDD, isso é aceitável porque começamos escrevendo um teste que falha e depois implementamos o mínimo necessário para fazê-lo passar. Inicialmente, `return 70` fazia o primeiro teste passar, mas era uma solução provisória. Quando criamos outro teste com valores diferentes, como `10, 15 e 25`, o retorno fixo não funcionou. Isso nos obrigou a implementar a soma real das três notas: `a1 + a2 + a3`.

### 2. No Ciclo 3, por que testar com 69 e 70, e não com 50 e 90?

Porque 69 e 70 são valores próximos ao limite mínimo de aprovação, que é 70. O teste com 69 verifica se o aluno é reprovado, enquanto o teste com 70 verifica se ele é aprovado. Assim, garantimos que a regra funciona exatamente no limite, evitando erros de comparação. Os valores 50 e 90 também seriam úteis, mas não verificariam o limite com a mesma precisão.

### 3. No Ciclo 4, o que mudou na refatoração? Como você teve certeza de que não quebrou nada?

Na refatoração, melhoramos a organização e a legibilidade do código, por exemplo, separando a validação das notas em um método privado chamado `validarNota()`. Isso evita repetição e facilita a manutenção. Tivemos certeza de que o comportamento continuava correto executando novamente todos os testes automatizados. Se todos continuassem passando, teríamos evidências de que a refatoração não alterou o comportamento esperado.

### 4. No Ciclo 8, por que alteramos os testes antes de mudar o código?

Porque, no TDD, os testes definem o comportamento esperado do sistema. Primeiro, alteramos ou criamos os testes para representar a nova regra de negócio. Depois, modificamos a implementação para atender a esses testes. Isso permite identificar o que precisa mudar e verificar se o código realmente cumpre os novos requisitos.

### 5. Qual ciclo foi o mais difícil para você, e por quê?

O ciclo mais difícil foi o da implementação da AI (Avaliação Integrada), porque foi necessário combinar várias regras: verificar a frequência, conferir se o aluno ainda não foi aprovado, avaliar a soma das notas e substituir a menor nota apenas quando a nota da AI fosse maior. Foi necessário pensar em diferentes situações e criar testes para garantir que todas essas condições fossem respeitadas.