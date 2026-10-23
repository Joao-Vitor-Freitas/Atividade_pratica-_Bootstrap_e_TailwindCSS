# Atividade_pratica-_Bootstrap_e_TailwindCSS

Atividade da FIAP em que o **mesmo layout** (protótipo "Empresa / Minha página") foi desenvolvido duas vezes: uma com **Bootstrap 5** e outra com **Tailwind CSS 3**. As duas versões têm os mesmos elementos e a mesma organização visual, para que seja possível comparar a experiência de desenvolvimento com cada tecnologia.

**Aluno:** João Vitor Dutra de Freitas |   **RM:** 573678

## Objetivo

Experimentar duas abordagens diferentes de CSS e compará-las na prática:

- **Bootstrap**: framework de componentes prontos (`container`, `row`, `col-*`, `btn`...).
- **Tailwind CSS**: framework utilitário, em que o visual é montado combinando classes pequenas direto no HTML (`px-4`, `bg-marca`, `rounded-full`...).

A análise crítica comparando as duas está no documento Word entregue junto com este repositório.

## Estrutura do repositório

| Branch | Conteúdo |
|---|---|
| `bootstrap` | Desenvolvimento da versão com Bootstrap |
| `tailwind` | Desenvolvimento da versão com Tailwind CSS |
| `main` | As duas versões finalizadas e este README |

```
.
├── README.md
├── bootstrap/
│   ├── index.html
│   ├── style.css
│   └── img/
└── tailwind/
    ├── index.html
    ├── style.css
    └── img/
```

## O layout

1. **Hero** com imagem de fundo e o título "EMPRESA" centralizado.
2. **Conteúdo principal**: título "Minha página", subtítulo, imagem de destaque e dois parágrafos.
3. **Seção cinza com 3 cards** (ClicRBS, Senac RS e Portal Terra), cada um com título, imagem, texto e botão arredondado. No celular os cards se empilham.

## Como cada versão foi construída

### Bootstrap (`bootstrap/`)

- Bootstrap 5.3.3 carregado por **CDN**.
- O layout usa o sistema de grid e utilitários do próprio Bootstrap: `container`, `row g-5`, `col-12 col-md-4`, `d-flex`, `py-5`, `rounded-pill`, `text-uppercase`...
- O `style.css` guarda o que o Bootstrap não traz pronto: a cor da marca (o botão `btn-brand` sobrescreve as variáveis `--bs-btn-*`), a fonte Arial, a largura de 1200px do container, a imagem de fundo do hero e os tamanhos de texto do protótipo.

### Tailwind CSS (`tailwind/`)

- Tailwind 3.4.17 carregado pelo **Play CDN**, sem etapa de build.
- Praticamente todo o estilo está nas classes do próprio HTML: `grid md:grid-cols-3`, `bg-fundo`, `rounded-full`, `hover:bg-marca-escuro`...
- A personalização (cores `marca`, `fundo` e `texto`, fonte Arial, largura máxima da página) é feita no bloco `tailwind.config` dentro do `index.html`.
- Valores que não existem na escala padrão usam *arbitrary values*, como `text-[1.3rem]` e `leading-[2.05]`.
- O `style.css` tem só a imagem de fundo do hero.

## Como executar

Não é preciso instalar nada: as duas versões usam CDN, então basta ter internet.

```bash
git clone https://github.com/Joao-Vitor-Freitas/Atividade_pratica-_Bootstrap_e_TailwindCSS.git
cd Atividade_pratica-_Bootstrap_e_TailwindCSS
```

Depois, abra no navegador (duplo clique ou "Open with Live Server" no VS Code):

- `bootstrap/index.html`
- `tailwind/index.html`

Para ver cada versão em desenvolvimento, troque de branch com `git checkout bootstrap` ou `git checkout tailwind`.
