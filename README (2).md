# Spazio Velluto

Site de página única (single page) do salão de beleza **Spazio Velluto**, da cabeleireira **Raissa Fischer**. O objetivo é apresentar os serviços e os preços e levar a cliente direto para o WhatsApp para agendar.

## Visão geral

- Página única com rolagem suave entre as seções.
- Visual claro, minimalista e feminino, com destaques em verde petróleo.
- Responsivo: funciona em celular, tablet e computador.
- Agendamento pelo WhatsApp, com mensagem pronta.

## Seções da página

| Seção | Conteúdo |
| --- | --- |
| Início | Nome do salão, frase de apresentação e botões "Agendar horário" e "Conheça nosso trabalho" |
| Atendimento | Horário de atendimento (segunda a sexta, 14h às 20h), endereço e WhatsApp |
| Serviços | Dez serviços em quatro grupos (Escova e corte; Tratamentos capilares; Progressiva e Botox; Retoques de raiz), cada um com preço e botão "Agendar". O Tratamento de Luxo é um card em destaque, com borda em verde petróleo, fundo diferenciado e preço maior |
| Diferencial | Seis pontos que guiam o atendimento |
| Galeria | Quatro fotos e quatro vídeos dos trabalhos, cada um com o nome do serviço logo abaixo |
| Depoimentos | Textos de exemplo, identificados como fictícios, para serem trocados por avaliações reais |
| Agendamento | Formulário (nome, serviço, data, horário e observação) que gera a mensagem do WhatsApp |
| Contato | Endereço, WhatsApp, Instagram e botão "Como chegar" (Google Maps) |
| Rodapé | Links para Instagram, WhatsApp e contato |

Também há três botões flutuantes: **Como me encontrar** (Google Maps), **Instagram** e **WhatsApp**.

## Tecnologias

- HTML5, CSS3 e JavaScript puro, sem frameworks e sem etapa de build.
- Tudo em um único arquivo, `index.html`: o CSS e o JavaScript ficam dentro dele.
- Fonte **Inter**, carregada do Google Fonts (é preciso internet para elas aparecerem; sem conexão o navegador usa uma fonte substituta).
- Ilustrações em SVG dentro do próprio código. As fotos e os vídeos da galeria ficam na pasta `midia/`, em formato original (JPEG e MP4).

## Estrutura do projeto

```
spazio-velluto/
├── index.html   # o site inteiro (HTML, CSS e JavaScript)
├── README.md    # este arquivo
└── midia/       # fotos, vídeos e capas dos vídeos da galeria
```

## Paleta de cores

| Cor | Código | Uso |
| --- | --- | --- |
| Branco quente | `#FAF9F6` | Fundo predominante |
| Bege muito claro | `#F1EEE7` | Fundos alternados |
| Verde-água suave | `#DDEFE8` | Faixas e detalhes em fundos |
| Verde petróleo | `#064B4D` | Botões, destaques e rodapé |
| Grafite esverdeado | `#263536` | Textos principais |
| Cinza suave | `#7B8580` | Contornos e detalhes discretos |

Os parágrafos secundários usam `#5E6A65`, um tom um pouco mais escuro que o cinza suave, para manter o contraste mínimo de leitura.

## Como funciona o WhatsApp

- Todos os links usam o formato `https://wa.me/5547984203311`.
- Os botões "Agendar" de cada serviço rolam até a seção de agendamento e já escolhem aquele serviço no formulário.
- O formulário de agendamento monta a mensagem com os dados preenchidos e abre o WhatsApp em uma nova aba.
- O botão flutuante e o botão "Chamar no WhatsApp" abrem a conversa com a mensagem "Olá, tudo bem? Gostaria de conhecer o seu trabalho".

## Como editar

Abra o `index.html` em um editor de texto e procure por:

- **Número do WhatsApp:** `5547984203311`. Ele aparece em vários links e na constante `WHATSAPP_NUMBER`, no final do arquivo. Troque em todos os lugares.
- **Preços:** aparecem uma única vez, na lista de serviços (`.menu-row`).
- **Serviços:** cada grupo é um bloco `.grupo` na seção `#servicos`, e cada serviço é uma linha `.menu-row`. Para incluir um serviço, copie uma linha existente e ajuste nome, preço e `data-service`. Inclua também o serviço na lista do formulário (`#servico`).
- **Card de destaque:** o Tratamento de Luxo usa a classe `.luxo`, no CSS e na lista de serviços.
- **Horário e endereço:** seções "Atendimento" e "Contato". O endereço também está nos links do Google Maps.
- **Instagram:** `instagram.com/spazio.velluto`.
- **Galeria:** cada trabalho é um bloco `<figure class="work">` na seção `#galeria`. O nome do serviço fica no `<figcaption>`. Para incluir outro, copie um bloco, coloque o arquivo em `midia/` e ajuste o caminho e o nome. Os vídeos têm uma capa (`video_N-poster.jpg`) na mesma pasta.
- **Depoimentos:** seção `#depoimentos`, hoje com textos de exemplo.
- **Cores:** variáveis no início do CSS, em `:root`.

## Como publicar

### GitHub Pages

1. Crie um repositório no GitHub (por exemplo, `spazio-velluto`).
2. Envie `index.html` e `README.md` para a raiz do repositório.
3. Vá em **Settings > Pages**.
4. Em **Source**, escolha **Deploy from a branch**, selecione a branch `main` e a pasta `/ (root)`, e salve.
5. Aguarde alguns minutos. O site ficará em `https://SEU-USUARIO.github.io/NOME-DO-REPOSITORIO/`.

Para atualizar o site depois, substitua o `index.html` no repositório e faça o commit.

### Netlify

1. Acesse [netlify.com](https://www.netlify.com) e entre na sua conta.
2. Em **Sites**, escolha **Add new site > Deploy manually**.
3. Arraste a pasta do projeto (com `index.html`) para a área de upload.
4. O site fica no ar em um endereço do Netlify, e é possível conectar um domínio próprio nas configurações do site.

## Contato do salão

- **WhatsApp:** +55 47 98420-3311
- **Instagram:** [@spazio.velluto](https://www.instagram.com/spazio.velluto/)
- **Endereço:** Rua Conde de Passé, 47 — Fortaleza, Blumenau - SC
- **Atendimento:** segunda a sexta, 14h às 20h
