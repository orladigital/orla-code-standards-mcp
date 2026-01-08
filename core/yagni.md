# YAGNI - Evitar Código sem Demanda Real

## Visão Geral

**YAGNI** (You Aren't Gonna Need It) é um princípio que enfatiza que você não deve adicionar funcionalidades até que sejam realmente necessárias.

## Princípio Fundamental

**Não implemente funcionalidades "por precaução" ou porque "pode ser útil no futuro".**

## Por Que YAGNI Importa

### Problemas de Violar YAGNI:
- **Código não utilizado** ocupa espaço e adiciona complexidade
- **Tempo desperdiçado** em funcionalidades que nunca serão usadas
- **Manutenção desnecessária** de código que não agrega valor
- **Overengineering** que dificulta mudanças futuras

## Quando Seguir YAGNI

### ✅ Siga YAGNI Quando:
- Você está tentando adicionar funcionalidade "por precaução"
- Não há requisito claro ou demanda real
- Você está antecipando necessidades futuras incertas
- A funcionalidade não resolve um problema atual

### ⚠️ Não Siga YAGNI Cegamente Quando:
- Há um requisito claro documentado
- A funcionalidade é parte de um roadmap aprovado
- Há evidência de que será necessária em breve
- A implementação é trivial e não adiciona complexidade

## Exemplos

### Exemplo 1: Funcionalidade Antecipada - Violar YAGNI

```typescript
// ❌ Violando YAGNI - funcionalidade não solicitada
class UserService {
  // Ninguém pediu suporte a múltiplos idiomas ainda
  createUser(data: UserData, language: string = 'pt-BR'): User {
    // Implementação complexa para suporte multi-idioma
    // que não será usado por meses (ou nunca)
  }
  
  // Ninguém pediu exportação CSV ainda
  exportToCSV(users: User[]): string {
    // Código que pode nunca ser usado
  }
}

// ✅ Seguindo YAGNI - apenas o necessário
class UserService {
  createUser(data: UserData): User {
    // Implementação simples e direta
  }
}
```

### Exemplo 2: Abstração Antecipada - Violar YAGNI

```typescript
// ❌ Violando YAGNI - abstração para caso futuro
interface PaymentProcessor {
  process(amount: number): Promise<PaymentResult>;
}

class CreditCardProcessor implements PaymentProcessor {
  // Implementação completa
}

// Mas só temos um método de pagamento hoje!

// ✅ Seguindo YAGNI - implementação direta
class PaymentService {
  async processCreditCard(amount: number): Promise<PaymentResult> {
    // Implementação direta, sem abstração desnecessária
  }
}

// Quando precisar de PayPal, aí sim criar a abstração
```

### Exemplo 3: Configuração Excessiva - Violar YAGNI

```typescript
// ❌ Violando YAGNI - configuração para casos não existentes
interface DatabaseConfig {
  host: string;
  port: number;
  ssl: boolean;
  connectionPool: number;
  retryAttempts: number;
  timeout: number;
  // ... 20 outras opções que nunca serão usadas
}

// ✅ Seguindo YAGNI - apenas o necessário
interface DatabaseConfig {
  host: string;
  port: number;
}
```

## YAGNI vs Planejamento

### YAGNI Não Significa:
- ❌ Não planejar o futuro
- ❌ Não pensar em arquitetura
- ❌ Não considerar escalabilidade

### YAGNI Significa:
- ✅ Não implementar código que não é necessário agora
- ✅ Não criar abstrações para problemas que não existem
- ✅ Não adicionar features "por precaução"

## Como Aplicar YAGNI

1. **Implemente apenas o que é necessário agora**
   - Resolva o problema atual
   - Não antecipe necessidades futuras

2. **Refatore quando necessário**
   - Quando a necessidade real surgir, refatore então
   - Código simples é mais fácil de refatorar

3. **Questione cada linha de código**
   - "Isso resolve um problema real agora?"
   - "Há demanda clara para isso?"

4. **Mantenha código simples**
   - Código simples é mais fácil de modificar quando necessário
   - Não precisa de funcionalidades "por precaução"

## Sinais de Violação de YAGNI

- Código comentado "para uso futuro"
- Interfaces/abstrações com apenas uma implementação
- Configurações que nunca são alteradas
- Funcionalidades que nunca são chamadas
- Comentários como "isso pode ser útil depois"

## YAGNI e Outros Princípios

- **YAGNI + KISS:** Mantenha simples e não adicione o que não precisa
- **YAGNI + DRY:** Não crie abstrações "por precaução" para eliminar duplicação futura
- **YAGNI + SOLID:** Aplique SOLID quando necessário, não antecipadamente

## Conclusão

**YAGNI é sobre focar no que importa agora.** Implemente funcionalidades quando há demanda real, não quando você acha que pode precisar no futuro. Código simples e direto é mais fácil de modificar quando a necessidade real surgir.
