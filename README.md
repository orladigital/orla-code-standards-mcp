# Orla Code Standards

Repositório centralizado de padrões e diretrizes de engenharia para toda a organização.

## 📋 Sobre

Este repositório define os padrões de engenharia de software que devem ser seguidos por todas as equipes da organização. Os padrões foram criados com base em princípios consagrados da indústria, aplicados de forma prática e pragmática ao nosso contexto.

## 🎯 Objetivo

Estabelecer uma base comum de conhecimento e práticas que:
- Garantem qualidade e consistência no código
- Facilitam a colaboração entre equipes
- Reduzem a curva de aprendizado para novos membros
- Promovem boas práticas de engenharia de software

## 📚 Estrutura

```
├── core/
│   ├── principles.md          # Princípios universais de engenharia
│   ├── solid.md               # SOLID aplicado de forma prática
│   ├── kiss.md                # Simplicidade acima de abstração
│   ├── dry.md                 # Reuso consciente (sem overengineering)
│   ├── yagni.md               # Evitar código sem demanda real
│   └── general-guidelines.md  # Diretrizes gerais
```

## 📖 Documentos

### [Princípios Universais](./core/principles.md)
Princípios fundamentais que guiam todas as decisões de engenharia na organização, incluindo qualidade, simplicidade, manutenibilidade e colaboração.

### [SOLID](./core/solid.md)
Aplicação prática dos cinco princípios SOLID (Single Responsibility, Open/Closed, Liskov Substitution, Interface Segregation, Dependency Inversion) com exemplos e quando aplicá-los.

### [KISS](./core/kiss.md)
Keep It Simple, Stupid - Diretrizes sobre quando escolher simplicidade sobre abstração complexa, com exemplos práticos.

### [DRY](./core/dry.md)
Don't Repeat Yourself - Aplicação consciente do princípio DRY, evitando overengineering e entendendo quando a duplicação é aceitável.

### [YAGNI](./core/yagni.md)
You Aren't Gonna Need It - Princípio que enfatiza não implementar funcionalidades até que sejam realmente necessárias.

### [Diretrizes Gerais](./core/general-guidelines.md)
Diretrizes gerais sobre estrutura de código, qualidade, processo de desenvolvimento, performance, segurança e trabalho em equipe.

## 🚀 Como Usar

1. **Leia os documentos** - Familiarize-se com os princípios e diretrizes
2. **Aplique no dia a dia** - Use os padrões como guia em code reviews e desenvolvimento
3. **Referencie em discussões** - Use os documentos como base para decisões técnicas
4. **Contribua** - Sugira melhorias e atualizações através de pull requests

## 💡 Princípios Fundamentais

1. **Qualidade sobre Velocidade** - Código de qualidade previne problemas futuros
2. **Simplicidade** - Prefira soluções simples e diretas
3. **Manutenibilidade** - Código será lido mais vezes do que escrito
4. **Colaboração** - Código é um produto de equipe
5. **Evolução Contínua** - Padrões evoluem com o tempo

## 🤝 Contribuindo

Contribuições são bem-vindas! Ao propor mudanças:

1. Abra uma issue discutindo a mudança proposta
2. Crie um pull request com as alterações
3. Explique o contexto e benefícios da mudança
4. Mantenha a consistência com o estilo e formato existente

## 📝 Notas Importantes

- **Não são regras rígidas** - Use bom senso e adapte ao contexto específico
- **Balance é fundamental** - Não sobre-engenhe, mas também não ignore padrões importantes
- **Evolução contínua** - Estes padrões devem evoluir com a organização
- **Pragmatismo** - Aplicação prática é mais importante que teoria pura

## 📞 Contato

Para dúvidas ou sugestões sobre os padrões, entre em contato com a equipe de engenharia ou abra uma issue neste repositório.

## ⚙️ Como instalar no Cursor

### Passo 1: Instalar as regras via Remote Rule

No Cursor, vá em:
```
Cursor > Settings > Cursor Settings > Rules and Commands > Project Rules > Remote Rule (github)
```

Cole a URL do repositório:
```
https://github.com/orladigital/orla-code-standards-mcp.git
```

### Passo 2: Localizar os arquivos baixados

O Cursor salvará automaticamente as regras em:
```
/Users/seu_usuario/.cursor/projects/seu_projeto/skills/orla-code-standards-mcp/
```

### Passo 3: Configurar o arquivo .cursorrules

1. **Copie o arquivo** [`.cursorrules`](./.cursorrules) deste projeto para a raiz do seu projeto
2. **Edite os caminhos** no arquivo copiado, substituindo `/Users/seu_usuario/.cursor/projects/seu_projeto` pelo caminho real onde as regras foram baixadas na sua máquina

### Passo 4: Personalizar (opcional)

O arquivo [`.cursorrules`](./.cursorrules) pode conter qualquer instrução adicional que você queira que o Cursor execute automaticamente, como:
- Ler arquivos de regras específicos
- Executar comandos personalizados
- Aplicar configurações específicas do projeto

### Passo 5: Escolher o escopo

**Opção A - Por projeto:** Mantenha o arquivo `.cursorrules` na raiz de cada projeto

**Opção B - Global:** Copie o conteúdo do arquivo e cole em:
```
Cursor > Settings > Cursor Settings > Rules and Commands > User Rules
```

