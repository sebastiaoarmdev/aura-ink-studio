# ✒️ Aura Ink Studio — Landing Page Premium

Uma Landing Page de alta conversão para um estúdio de tatuagem fictício de alto padrão, focada no direcionamento de leads qualificados para o WhatsApp. Desenvolvida seguindo os padrões mais rígidos de **Código Limpo (Clean Code)**, **Semântica HTML5**, **Acessibilidade (a11y)** e **Web Performance**.

🚀 **[Acesse o projeto rodando ao vivo aqui](https://seu-usuario.github.io/aura-ink-studio/)**

---

## 🎯 Objetivo do Projeto
O projeto foi desenhado para simular um produto real entregue a um cliente de nicho *Premium*. O foco central é a experiência do usuário (UX) no ecossistema mobile, garantindo que a página carregue instantaneamente mesmo sob conexões de rede limitadas (3G/4G), eliminando atritos na conversão final para o WhatsApp.

---

## 🛠️ Tecnologias e Técnicas Utilizadas

- **HTML5 Semântico:** Uso rigoroso de tags estruturais (`<main>`, `<section>`, `<article>`, `<details>`) para garantir SEO otimizado e indexação precisa pelos motores de busca.
- **CSS3 Moderno Puro:** Arquitetura construída sem a necessidade de frameworks ou pré-processadores. 
  - Uso de **CSS Variables** (Custom Properties) para um Design System centralizado e de fácil manutenção.
  - **CSS Grid & Flexbox Layouts** totalmente responsivos e fluidos *sem a dependência excessiva de Media Queries*.
  - Tipografia fluida aplicando a função nativa `clamp()`.
- **Performance de Mídia (Imagens):** 
  - Renderização condicional de formatos de última geração (`.avif` e `.webp`) via elemento `<picture>`.
  - Técnicas nativas de `loading="lazy"` e `decoding="async"` para otimização de carregamento (Core Web Vitals).
- **Acessibilidade (a11y):** Implementação de links rápidos de salto para teclados (`sr-only`), atributos `aria-*` adequados para tecnologias assistivas (leitores de tela) e contraste de cores validado.

---

## 📐 Decisões de Arquitetura e Engenharia (Os Porquês)

### 1. Zero JavaScript para Componentes Interativos
O componente de perguntas frequentes (FAQ) foi desenvolvido utilizando puramente as tags nativas `<details>` e `<summary>`. O gerenciamento de estado (aberto/fechado) e a acessibilidade via teclado são controlados diretamente pelo navegador. 
* **O Ganho:** Economia de bytes preciosos de JavaScript, melhorando a métrica TBT (Total Blocking Time) e eliminando problemas de hidratação ou travamentos na renderização.

### 2. Layout Sem Saltos (CLS Zero)
Todas as imagens da galeria possuem atributos explícitos de `width` e `height`, combinados com a propriedade CSS `aspect-ratio: 4 / 5`. 
* **O Ganho:** O navegador reserva o espaço exato da imagem antes mesmo dela ser baixada, zerando o indicador CLS (Cumulative Layout Shift) e garantindo uma experiência de rolagem suave.

### 3. Design System Centralizado
Toda a paleta de cores (Dark Minimalist), transições e espaçamentos estão ancorados na pseudo-classe `:root`.
* **O Ganho:** Manutenibilidade. Caso o cliente mude a identidade visual do estúdio, a alteração de duas variáveis no arquivo CSS reflete globalmente e de forma consistente em toda a página.

---

## 📂 Estrutura de Pastas
```text
aura-ink-studio/
├── assets/
│   ├── images/       # Imagens otimizadas (AVIF/WebP)
│   └── css/          # Estilos globais (style.css)
├── index.html        # Estrutura semântica do projeto
├── README.md         # Documentação da aplicação
└── LICENSE           # Licença MIT
