# Viaggeuro

Controle de gastos para viagens, com foco no euro. Você define um teto de gastos por categoria e, a cada gasto lançado, o app mostra quanto já gastou e quanto ainda pode gastar no dia e na viagem toda.

Feito para uso no celular (Android), em tema escuro e **sem internet** depois de instalado.

## O que o app faz

- **Tetos por categoria:** total da viagem e, opcionalmente, diário. As categorias padrão são Alimentação, Transporte, Telefonia/Internet, Hospedagem e Outros, e podem ser editadas.
- **Lançamento rápido:** botão "+", teclado numérico e escolha da categoria com um toque.
- **Acompanhamento:** gasto acumulado, quanto ainda dá para gastar e a porcentagem usada, por dia, por categoria e no total.
- **Cores de alerta:** verde abaixo de 70% do teto, amarelo de 70% a 100%, vermelho quando o teto é ultrapassado.
- **Média disponível:** quanto ainda dá para gastar por dia nos dias que faltam.
- **Histórico:** gastos agrupados por dia, com filtro por categoria. Tocar num gasto permite editar ou excluir.
- **Backup:** exportar e importar os dados em um arquivo `.json`.

## Privacidade

- Não pede login, nome, e-mail nem nenhum dado pessoal.
- Os gastos ficam salvos **somente no aparelho** de quem usa, no armazenamento local do navegador.
- O app não envia dados para nenhum servidor. Cada pessoa que usa o link tem os próprios dados, e ninguém vê os de ninguém.
- Este repositório contém apenas o código do app. Nenhum gasto fica aqui.

## Como instalar no Android

1. Abra o link do app (na seção **About** deste repositório) no **Chrome**.
2. Toque no menu **⋮** e depois em **Instalar app** (ou **Adicionar à tela inicial**).
3. Abra o app pelo ícone e configure os tetos em **Ajustes**.
4. Para testar sem internet: ative o modo avião e abra o app de novo.

Dica: faça um backup de vez em quando em **Ajustes → Exportar backup**.

## Como funciona

É um PWA (Progressive Web App) feito com HTML, CSS e JavaScript puros, sem bibliotecas nem dependências externas.

| Arquivo | Função |
|---|---|
| `index.html` | O app: interface, estilos e lógica |
| `manifest.webmanifest` | Permite instalar o app na tela inicial |
| `sw.js` | Guarda o app no aparelho para funcionar sem internet |
| `icon-192.png`, `icon-512.png` | Ícones |

Para publicar uma versão nova, altere os arquivos e troque o nome do cache em `sw.js` (por exemplo, de `orcviagem-v1` para `orcviagem-v2`). Os celulares recebem a atualização na próxima vez que abrirem o app com internet, sem perder os dados.

## Autoria

Projeto desenvolvido em coautoria com IA (Claude, da Anthropic): eu defini o problema, os requisitos e as decisões de produto, e o código foi gerado e revisado em conjunto com a IA.
