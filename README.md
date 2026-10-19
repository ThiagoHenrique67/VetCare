🐾 VetCare — Hospital Veterinário e Centro Diagnóstico

Projeto desenvolvido como simulação de ambiente profissional front-end para o Hospital Veterinário VetCare, focando em boas práticas de arquitetura, semântica, acessibilidade e responsividade.

📌 Visão Geral e Objetivo do Projeto

O VetCare é um hospital veterinário fictício que oferece atendimento especializado e pronto atendimento 24 horas para cães, gatos e animais silvestres.

O objetivo principal deste projeto é aplicar conceitos avançados de desenvolvimento front-end semântico, construindo uma interface fluida, moderna, acessível e totalmente responsiva para tutores de animais de estimação que buscam serviços médicos especializados.

🚀 Tecnologias e Conceitos Aplicados

HTML5 Semântico: Utilização correta de tags estruturais (<header>, <nav>, <main>, <section>, <article>, <details>, <summary>, <footer>) garantindo acessibilidade e bom SEO.

CSS3 Modular & Design System:

Variáveis CSS (Tokens): Centralização de cores, fontes, sombras e espaçamentos no :root.

Escala REM & Ajuste de Raiz: Configuração da escala base de fonte em porcentagem no elemento raiz (html) e uso estrito de unidades rem para tipografia, bordas e espaçamentos.

Layouts Flexíveis: Uso de Flexbox para alinhamento e distribuição de cards, menus e seções.

Unidades de Layout: Emprego de porcentagens (%), vh e vw para controle de dimensões e visualização em tela cheia (Full Screen Layout).

Metodologia BEM (Block Element Modifier): Nomenclatura rigorosa de classes CSS (bloco__elemento--modificador) garantindo baixo acoplamento e reuso de estilos.

Responsividade Fluida: Adaptação do layout para dispositivos móveis, tablets e desktops através de media queries com breakpoints estruturados.

Microinterações & Pseudo-classes: Transições suaves (transition), sombras interativas (box-shadow) e transformações (transform) nos estados :hover.

Recursos Externos & APIs:

Google Fonts: Importação e aplicação da família tipográfica Poppins (pesos 400, 500, 600 e 700).

WhatsApp API: Botão flutuante integrado à URL oficial do WhatsApp direcionado ao atendimento oficial da Escola SENAI Henrique Lupo.

Placehold.co & Unsplash: Imagens temáticas otimizadas para apresentação do hospital.

🎨 Design System e Tokens CSS

As cores e estilos do projeto foram estruturados seguindo a identidade visual Saúde Animal:

:root {
  /* Paleta de Cores Principais */
  --color-bg-main: #f0fdf4;
  --color-bg-card: #ffffff;
  --color-sidebar-bg: #064e3b;
  --color-sidebar-text: #ecfdf5;
  --color-primary: #059669;
  --color-primary-hover: #047857;
  --color-secondary: #0d9488;
  --color-accent: #f59e0b;

  /* Textos e Bordas */
  --color-text-title: #022c22;
  --color-text-body: #1f2937;
  --color-text-muted: #4b5563;
  --color-border: #d1fae5;

  /* Tipografia */
  --font-main: 'Poppins', system-ui, -apple-system, sans-serif;
  --font-size-sm: 1.4rem;
  --font-size-base: 1.6rem;
  --font-size-lg: 2rem;
  --font-size-xl: 3.2rem;

  /* Efeitos e Sombras */
  --shadow-card: 0 10px 20px -5px rgba(5, 150, 105, 0.15);
  --shadow-hover: 0 15px 30px -5px rgba(5, 150, 105, 0.3);
  --radius-sm: 0.8rem;
  --radius-md: 1.6rem;
  --transition: all 0.3s ease-in-out;
}


🏛️ Estrutura das Seções e Requisitos Funcionais

Menu Lateral Esquerdo Fixo (position: fixed):

Navegação contínua na versão desktop com suporte a rolagem suave (scroll-behavior: smooth) e compensação de recuo de âncora.

Seção 1 — Hero / Boas-vindas (#home):

Apresentação institucional ocupando 100% da área visível (100vh), destacando o compromisso com o cuidado animal.

Seção 2 — Especialidades Médicas (#especialidades):

Exibição de cards estilizados com Flexbox cobrindo Cardiologia Veterinária, Ortopedia e Traumatologia e Dermatologia Especializada.

Seção 3 — Corpo Clínico (#equipe):

Apresentação dos veterinários responsáveis, com foto, nome, registro profissional (CRMV) e especialidade.

Seção 4 — Infraestrutura e Atendimento (#infraestrutura):

Informações sobre o centro cirúrgico, UTI, laboratório e quadro informativo dos horários de atendimento (Pronto Atendimento 24h e Consultas).

Seção 5 — FAQ Interativo (#faq):

Perguntas frequentes implementadas de forma nativa e acessível utilizando as tags <details> e <summary>.

Rodapé Fixo (position: fixed):

Exibição permanente de localização e informações de direitos autorais.

Botão Flutuante do WhatsApp:

Posicionado de forma fixa no canto inferior direito, com redirecionamento direto via API para o número da instituição.

📁 Arquitetura de Arquivos

A organização do projeto segue o princípio de separação rigorosa de responsabilidades sem o uso de estilos inline ou blocos <style> embutidos no HTML:

vetcare-hospital/
├── index.html              # Estrutura HTML5 semântica da aplicação
├── css/
│   ├── variables.css      # Variáveis globais do Design System (:root)
│   ├── reset.css          # Reset de margens e configuração da escala REM
│   ├── components.css     # Estilos de cards, botões, FAQ e elementos
│   └── style.css          # Estilos principais, layout, sidebar e media queries
├── assets/
│   └── images/            # Imagens e ícones utilizados no projeto
└── README.md              # Documentação oficial do projeto


💡 Desafios Técnicos e Aprendizados

Alinhamento e Compensação da Sidebar: A utilização de uma navegação lateral fixa (position: fixed) exigiu o ajuste preciso de margens e espaçamentos (margin-left e padding-top) nas seções principais para evitar a sobreposição do conteúdo e garantir que o scroll de âncora direcionasse a página corretamente.

Consistência do REM e Escala Raiz: Garantir que 100% da tipografia, paddings e bordas utilizassem unidades relativas rem, configurando a proporção de fonte base no html e resgatando a escala no body.

Rigor na Metodologia BEM: Manter a consistência das classes em uma estrutura com múltiplos cards e seções exigiu disciplina na modelagem dos elementos e modificadores CSS.

Uso Nativo de <details> e <summary>: Estilização semântica do componente FAQ garantindo boa usabilidade e acessibilidade sem dependência de scripts adicionais.

💻 Como Visualizar e Executar o Projeto

Clonar o Repositório:

git clone https://github.com/seu-usuario/vetcare-hospital.git


Navegar até a pasta do projeto:

cd vetcare-hospital


Executar a aplicação:

Basta abrir o arquivo index.html em qualquer navegador web de sua preferência.

Alternativamente, utilize a extensão Live Server no VS Code para simular um servidor local com recarregamento automático.

📜 Licença e Créditos

Este projeto foi desenvolvido para fins educacionais de acordo com o documento de orientações do curso.

Cliente Fictício: VetCare — Hospital Veterinário e Centro Diagnóstico

Instituição de Ensino: Escola SENAI Henrique Lupo — Araraquara/SP

Desenvolvido por: [Thiago Henrique]
