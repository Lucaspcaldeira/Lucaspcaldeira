## Lucas Caldeira

**Assistente de Programador Fullstack** · Estudante de Ciência da Computação

No trabalho: **.NET Core**, **Vue.js**, JavaScript e **CQRS**.

Aqui no GitHub costuma aparecer outra coisa — C, jogos, hardware antigo. É de
propósito: gosto de problema em que a restrição é real e não dá para resolver
instalando um pacote. Pouca memória, tela pequena, formato mal documentado.

---

### 📖 [psp-reader](https://github.com/Lucaspcaldeira/psp-reader) — leitor de EPUB, PDF e TXT para PlayStation Portable

O PSP tem 480x272 de tela e 64 MB de RAM. Uma página A4 reduzida para caber
deixa o texto com 4 pixels — ilegível. Então o leitor não encolhe a página: ele
**extrai o texto, reconstrói os parágrafos e repagina** para a tela, como um
Kindle faz.

A licença MIT eliminou as bibliotecas óbvias — MuPDF é AGPL, Bookr é GPLv2 — o
que obrigou a escrever o parser de PDF, o leitor de ZIP/EPUB e o motor de reflow
do zero. A restrição acabou levando a uma arquitetura melhor: a camada de
leitura inteira é C99 puro sobre uma interface de I/O de três funções, compila
no PC e é exercitada por **497 asserções** com AddressSanitizer e
UndefinedBehaviorSanitizer — sem precisar do console para achar um bug.

Dois defeitos que os testes pegaram e a inspeção não teria pegado: um laço
infinito na leitura do diretório central do ZIP, e um parágrafo que sumia na
emenda entre trechos de um capítulo grande.

`C` · `PSPSDK` · `FreeType` · `zlib` · CI no GitHub Actions · testado em hardware real

---

### Outros projetos

| | |
|---|---|
| [Frog](https://github.com/Lucaspcaldeira/Frog) | Jogo estilo Frogger em p5.js, com colisão, placar e trilha |
| [Pong](https://github.com/Lucaspcaldeira/Pong) | Pong em p5.js com oponente automático e efeitos sonoros |
| [sistema-de-cadastro](https://github.com/Lucaspcaldeira/sistema-de-cadastro) | Cadastro de jogos em Node.js, em desenvolvimento |

---

### No que estou mexendo

Trazendo para cá projetos mais próximos do que faço no dia a dia — back-end em
.NET Core e front-end em Vue — sem largar o lado de baixo nível, que é onde
aprendo mais rápido.

---

[LinkedIn](https://www.linkedin.com/in/lscaldeira/) · lscaldeira@outlook.com
