# SOLID - Aplicado de Forma Prática

## Visão Geral

SOLID são cinco princípios de design orientado a objetos que tornam o software mais compreensível, flexível e manutenível.

## S - Single Responsibility Principle (Princípio da Responsabilidade Única)

**Definição:** Uma classe deve ter apenas uma razão para mudar.

**Aplicação Prática:**
- Cada classe/função deve ter uma única responsabilidade bem definida
- Se uma classe faz muitas coisas diferentes, considere dividi-la

**Exemplo:**
```typescript
// ❌ Ruim - múltiplas responsabilidades
class User {
  save() { /* salva no banco */ }
  sendEmail() { /* envia email */ }
  validate() { /* valida dados */ }
}

// ✅ Bom - responsabilidade única
class User {
  validate() { /* valida dados */ }
}

class UserRepository {
  save(user: User) { /* salva no banco */ }
}

class EmailService {
  sendWelcomeEmail(user: User) { /* envia email */ }
}
```

## O - Open/Closed Principle (Princípio Aberto/Fechado)

**Definição:** Entidades devem estar abertas para extensão, mas fechadas para modificação.

**Aplicação Prática:**
- Use interfaces e abstrações para permitir extensão sem modificar código existente
- Evite modificar classes existentes quando adicionar novas funcionalidades

## L - Liskov Substitution Principle (Princípio da Substituição de Liskov)

**Definição:** Objetos de uma superclasse devem ser substituíveis por objetos de suas subclasses sem quebrar a aplicação.

**Aplicação Prática:**
- Subclasses devem poder substituir suas classes base sem alterar o comportamento esperado
- Mantenha contratos consistentes entre classes base e derivadas

## I - Interface Segregation Principle (Princípio da Segregação de Interface)

**Definição:** Clientes não devem ser forçados a depender de interfaces que não utilizam.

**Aplicação Prática:**
- Crie interfaces específicas e focadas
- Evite interfaces "gordas" que forçam implementação de métodos não utilizados

## D - Dependency Inversion Principle (Princípio da Inversão de Dependência)

**Definição:** Dependa de abstrações, não de implementações concretas.

**Aplicação Prática:**
- Use injeção de dependência
- Dependa de interfaces/contratos, não de implementações específicas

## Quando Aplicar SOLID

- **Aplique quando:** O código será mantido por longo prazo ou por múltiplas pessoas
- **Não aplique quando:** Está criando um protótipo rápido ou código descartável
- **Balance:** Não sobre-engenhe. SOLID deve facilitar, não complicar.
