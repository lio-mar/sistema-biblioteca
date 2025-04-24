# sistema-biblioteca

# Identificação de Violações SOLID e Clean Code

# 1. Violação do SRP (Single Responsibility Principle)

**Classe/Método**: GerenciadorBiblioteca (toda a classe)

**Problema**: A classe tem múltiplas responsabilidades (gerenciar livros, usuários, empréstimos, notificações e cálculo de multas)

**Justificativa**: Uma classe deve ter apenas um motivo para mudar. Neste caso, a classe está fazendo coisas demais, o que torna difícil de manter e testar.

# 2. Violação do OCP (Open/Closed Principle)

**Classe/Método**: GerenciadorBiblioteca (métodos de notificação)

**Problema**: Se precisarmos adicionar um novo tipo de notificação (ex: push notification), precisamos modificar a classe existente.

**Justificativa**: O princípio diz que classes devem estar abertas para extensão, mas fechadas para modificação. Deveríamos poder adicionar novos comportamentos sem alterar o código existente.

# 3. Violação do DIP (Dependency Inversion Principle)

**Classe/Método**: GerenciadorBiblioteca (métodos EnviarEmail e EnviarSMS)

**Problema**: A classe depende de implementações concretas de notificação em vez de abstrações.

**Justificativa**: Depender de abstrações (interfaces) em vez de implementações concretas permite maior flexibilidade e facilita testes unitários.

# 4. Violação do Clean Code (Funções grandes)

**Classe/Método**: GerenciadorBiblioteca.RealizarEmprestimo e RealizarDevolucao

**Problema**: Métodos fazem muitas coisas (lógica de negócio, alteração de estado e notificações)

**Justificativa**: Métodos devem ser pequenos e fazer apenas uma coisa, o que melhora legibilidade e manutenção.

# 5. Violação do Clean Code (Nomes pouco descritivos)

**Classe/Método**: Variável var l = new Livro() e var u = new Usuario()

**Problema**: Nomes de variáveis muito curtos e não descritivos

**Justificativa**: Nomes devem revelar a intenção do código, tornando-o mais legível e auto-documentado.
