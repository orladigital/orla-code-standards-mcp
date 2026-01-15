# DRY - Reuso Consciente (Sem Overengineering)

## Visão Geral

**DRY** (Don't Repeat Yourself) é um princípio que visa reduzir a repetição de código. No entanto, deve ser aplicado com sabedoria, evitando overengineering.

## Princípio Fundamental

**Cada pedaço de conhecimento deve ter uma representação única, não ambígua e autoritativa dentro de um sistema.**

## Quando Aplicar DRY

### ✅ Aplique DRY Quando:
- Há **duplicação real** de lógica de negócio
- A duplicação causa **problemas de manutenção** (bugs em múltiplos lugares)
- O código duplicado é **significativo** (não apenas algumas linhas)
- A abstração resultante é **clara e compreensível**

### ❌ Não Aplique DRY Quando:
- A duplicação é **acidental** (código similar mas com propósitos diferentes)
- A abstração resultante seria **menos clara** que a duplicação
- Você está **antecipando** necessidades futuras
- A duplicação é **trivial** (2-3 linhas simples)

## Exemplos

### Exemplo 1: Duplicação Real - Aplicar DRY

```typescript
// ❌ Duplicação real - mesma lógica em múltiplos lugares
function validateEmail(email: string): boolean {
  const regex = /^[^\s@]+@[^\s@]+\.[^\s@]+$/;
  return regex.test(email);
}

function checkUserEmail(email: string): boolean {
  const regex = /^[^\s@]+@[^\s@]+\.[^\s@]+$/;
  return regex.test(email);
}

// ✅ DRY aplicado corretamente
function validateEmail(email: string): boolean {
  const regex = /^[^\s@]+@[^\s@]+\.[^\s@]+$/;
  return regex.test(email);
}

function checkUserEmail(email: string): boolean {
  return validateEmail(email);
}
```

### Exemplo 2: Duplicação Acidental - Não Aplicar DRY

```typescript
// ✅ Duplicação acidental - propósitos diferentes
function calculateCircleArea(radius: number): number {
  return Math.PI * radius * radius;
}

function calculatePizzaPrice(diameter: number): number {
  const radius = diameter / 2;
  return Math.PI * radius * radius * PRICE_PER_SQUARE_INCH;
}

// Não force uma abstração aqui - são contextos diferentes
```

### Exemplo 3: Overengineering - Evitar

```typescript
// ❌ Overengineering - abstração desnecessária
class NumberMultiplier {
  multiply(a: number, b: number): number {
    return a * b;
  }
}

// ✅ Simples e direto
const result = a * b;
```

## Regras de Ouro

1. **Duplicação de código ≠ Duplicação de conhecimento**
   - Código similar pode representar conceitos diferentes
   - Não force abstrações quando os contextos são diferentes

2. **Prefira duplicação sobre abstração ruim**
   - Se a abstração não é clara, mantenha a duplicação
   - Você sempre pode refatorar depois quando o padrão ficar claro

3. **Aplique DRY progressivamente**
   - Não tente eliminar toda duplicação de uma vez
   - Refatore quando a duplicação causar problemas reais

4. **Considere o custo de manutenção**
   - Se abstrair aumenta a complexidade, pode não valer a pena
   - Avalie o trade-off entre duplicação e complexidade

## Sinais de Overengineering com DRY

- Abstrações que são mais difíceis de entender que o código original
- Múltiplas camadas de indireção para eliminar duplicação trivial
- Código genérico que tenta resolver problemas que não existem
- Parâmetros complexos para tornar código "reutilizável"

## DRY vs WET

**WET** (Write Everything Twice) é às vezes preferível quando:
- A duplicação é mínima e clara
- A abstração seria confusa
- Os contextos são fundamentalmente diferentes

## Conclusão

DRY é uma ferramenta poderosa, mas deve ser aplicada com sabedoria. **Reuso consciente significa saber quando NÃO aplicar DRY tanto quanto saber quando aplicá-lo.** A meta é código manutenível, não código sem duplicação a qualquer custo.
