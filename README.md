# Agência Criativa Web

Página institucional de uma agência fictícia, desenvolvida para a atividade de design responsivo da EBAC.

## Executar

Abra `index.html` no navegador ou utilize a extensão Live Server do VS Code. Não há dependências nem etapa de compilação.

## Conteúdo e técnicas

- HTML5 semântico: header, nav, main, section, article, figure, address e footer.
- Home, Sobre Nós, Serviços, Depoimentos e Contato.
- Flexbox no menu e CSS Grid nos serviços e nas demais composições.
- Unidades relativas: %, rem, em, vw, vh e fr.
- Media queries para celular, tablet e desktop; menu reorganizado sem depender de JavaScript.
- Imagem local em três tamanhos, com srcset, sizes, dimensões explícitas e carregamento tardio.
- Links internos, telefone e e-mail; campos com rótulos e validação HTML nativa.
- Formulário demonstrativo com retorno na página; não envia nem armazena dados.
- Foco visível, link para pular navegação e respeito à preferência por movimento reduzido.

## Imagem

Fotografia de equipe: Annie Spratt / Unsplash, https://unsplash.com/photos/QckxruozjRg . Variantes locais de 480, 960 e 1440 pixels.

## Conteúdo fictício

Agência, depoimentos e dados de contato são demonstrativos. O domínio `.example` é reservado para exemplos.

## Conferência manual

No modo responsivo do navegador, conferir 375 × 812, 768 × 1024 e 1440 × 900: ausência de rolagem horizontal, legibilidade, reorganização do menu e grids, links de navegação e validação do formulário. Testar envio vazio, e-mail inválido e preenchimento válido; somente o último deve exibir a confirmação da demonstração.

## Publicação

Repositório público: https://github.com/math-giannotti18/agencia-criativa-web . Todos os arquivos, incluindo a pasta `imagens`, fazem parte da entrega. Para usar GitHub Pages, selecione a branch principal e a pasta raiz nas configurações de Pages do repositório.

## Verificação realizada

Página conferida no Chrome em 375 × 812, 768 × 1024 e 1440 × 900. Sem rolagem horizontal; todos os destinos de navegação encontrados; imagens carregadas; serviços em uma, duas e quatro colunas, respectivamente. Validação de campos vazios, e-mail inválido e confirmação demonstrativa verificada nas três resoluções.

## Refatoração CSS com BEM

A atividade de manutenção preserva o site do módulo anterior: nenhum conteúdo, seção, cálculo ou comportamento foi acrescentado.

### Convenção de classes

- Bloco: componente independente, como `.servico`, `.botao` ou `.formulario`.
- Elemento: parte do bloco, como `.servico__titulo`, `.botao__icone` e `.formulario__campo`.
- Modificador: variação utilizada junto da classe base, como `.botao.botao--escuro`, `.avatar.avatar--roxo` e `.formulario__campo.formulario__campo--mensagem`.
- Componentes compartilhados: `.container`, `.secao`, `.etiqueta`, `.logo`, `.botao`, `.avatar`, `.selo` e `.valores`.

O arquivo `estilos.css` está dividido em estilos gerais, componentes reutilizáveis, seções e regras responsivas. Seletores de apresentação usam classes diretas, sem dependência da posição dos elementos ou de tags descendentes. As regras globais de tags ficam restritas à normalização e aos padrões básicos da página.

O antigo seletor `#form-status` foi substituído por `.formulario__status`. IDs continuam no HTML apenas para âncoras, rótulos, acessibilidade e referências do JavaScript. Modificadores e elementos não exigem seletores encadeados: `.servico__titulo` possui especificidade de uma classe.

Declarações compartilhadas foram agrupadas, incluindo campos do formulário, nome/cargo dos depoimentos e textos do rodapé. As media queries e os estados de foco e interação foram preservados.

### Validação da refatoração

Comparação automatizada no Chrome, antes e depois, em **375 × 812**, **768 × 1024** e **1440 × 900**:

- Capturas de página inteira idênticas em cada resolução.
- Nenhuma diferença nos estilos calculados dos elementos.
- Textos e imagens preservados; nenhuma rolagem horizontal.
- Destinos dos links internos e validação do formulário conferidos.
- Campos vazios e e-mail inválido rejeitados; confirmação demonstrativa e limpeza da mensagem após edição preservadas.

### Prints para a entrega

A pasta `prints/` contém três capturas de página inteira, prontas para anexar na plataforma do curso:

- [Celular — 375 × 812](prints/celular-375.png)
- [Tablet — 768 × 1024](prints/tablet-768.png)
- [Desktop — 1440 × 900](prints/desktop-1440.png)
