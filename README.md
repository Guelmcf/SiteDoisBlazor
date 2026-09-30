# SiteDoisBlazor

Lista de exercícios práticos de **Blazor Nível 2 (Interatividade + Navegação)**, desenvolvida para a disciplina de **Desenvolvimento Web** (Usabilidade, Dev. Web, Mobile e Jogos) do professor Daniel Henrique Matos de Paiva.

O projeto reúne três páginas interativas em Blazor, todas acessíveis pelo menu lateral da aplicação.

## Tecnologias

- .NET / C#
- Blazor Web App com renderização `InteractiveServer`
- Bootstrap (layout padrão do template)

## Páginas

| Página | Rota | O que faz |
|---|---|---|
| Conversor de Temperatura | `/conversor` | Converte um valor em Celsius para Fahrenheit |
| Calculadora de Média | `/media` | Calcula a média de duas notas e indica se o aluno foi aprovado ou reprovado |
| Sorteador de Números | `/sorteio` | Gera um número aleatório entre 1 e 100 |

### Exercício 1: Conversor de Temperatura

Pratica o uso de `@bind` em formulários e de `@onclick` em botões.

- O usuário digita a temperatura em Celsius.
- O método `Converter` aplica a fórmula `F = (C × 9/5) + 32`.
- O resultado aparece como **Temperatura em Fahrenheit: X °F**.

### Exercício 2: Calculadora de Média do Aluno

Trabalha com múltiplos inputs, tipos anuláveis e renderização condicional.

- Dois campos numéricos recebem as notas (`nota1` e `nota2`).
- O método `CalcularMedia` calcula a média aritmética e a guarda em uma variável `double?`, que começa nula.
- O resultado só aparece depois do primeiro cálculo:
  - média maior ou igual a 7.0: **Aprovado!** em verde
  - média menor que 7.0: **Reprovado!** em vermelho

### Exercício 3: Sorteador de Números

Usa a classe `System.Random` dentro de um método de evento do Blazor.

- O botão **Gerar Número Aleatório** chama o método `SorteiaNumero`.
- O número sorteado (de 1 a 100) é exibido em um `<h2>`.

### Exercício 4: Menu de Navegação

As três páginas foram adicionadas ao `NavMenu.razor` com o componente `<NavLink>`, então dá para navegar entre elas pela barra lateral sem digitar a URL.

## Como executar

Pré-requisito: [.NET SDK](https://dotnet.microsoft.com/download) instalado.

```bash
# clonar o repositório
git clone https://github.com/SEU-USUARIO/site-dois-blazor.git
cd site-dois-blazor

# executar com hot reload
dotnet watch
```

Também é possível abrir a solução no Visual Studio e executar com **F5**.

## Estrutura

```
SiteDoisBlazor/
├── Components/
│   ├── Layout/
│   │   └── NavMenu.razor      # menu lateral com os links das páginas
│   └── Pages/
│       ├── Conversor.razor    # /conversor
│       ├── Media.razor        # /media
│       └── Sorteio.razor      # /sorteio
└── Program.cs
```

## Equipe

- Miguel Figueiredo (ra: 125111399767)


## Licença

Este projeto está sob a licença MIT. Veja o arquivo [LICENSE](LICENSE) para mais detalhes.
