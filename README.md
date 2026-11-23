# Apresentação — SOH Prediction via Global Degradation Priors and Residual Learning

Pacote de apresentação Beamer em 16:9, construído sobre o `Template_CINE.zip`
fornecido pelo usuário e preenchido com conteúdo e figuras da pasta-fonte do paper.

## Conteúdo

- `main.tex`: fonte LaTeX da apresentação (12 slides, em inglês).
- `beamerthemeResearchUNIFESP.sty`: tema institucional original do template.
- `assets/logos/`: logotipos CINE, UNIFESP e CIDAG.
- `figures/`: figuras originais selecionadas da pasta `Figures/reduced` do paper.
- `presentation.pdf`: PDF compilado da apresentação.
- `paper_source/paper_main.tex`: fonte LaTeX do artigo utilizada para extrair os tópicos.
- `paper_source/biblio.bib`: bibliografia do artigo.
- `build.sh`: script de compilação local.

## Compilação no Ubuntu

Instale os pacotes necessários (caso ainda não estejam instalados):

```bash
sudo apt install texlive-latex-extra latexmk
```

Depois, na raiz da pasta:

```bash
./build.sh
```

Ou diretamente:

```bash
pdflatex -interaction=nonstopmode main.tex
pdflatex -interaction=nonstopmode main.tex
```

## Estrutura da apresentação

1. Title
2. Motivation
3. Central hypothesis
4. Datasets and SOH definition
5. Population-level degradation prior
6. Residual learning and hybrid SVR
7. Experimental protocol
8. Wenzhou results
9. HNEI results
10. Qualitative analysis
11. Discussion and limitations
12. Conclusions and acknowledgements

## Observações científicas importantes

- O SOH é definido no paper como `C_c / C_0`, com `C_0` sendo a capacidade no primeiro ciclo retido.
- A representação compartilhada utiliza a curva média e sua primeira diferença discreta.
- A avaliação utiliza LOBO externo e LOBO interno para seleção de hiperparâmetros.
- O MAE é calculado somente nos ciclos futuros, não utilizados no ajuste.
- A tabela quantitativa principal compara a curva média com o SVR residual híbrido.
  O baseline de SVR individual é apresentado qualitativamente no paper; a apresentação
  preserva essa distinção.
- As comparações com métodos publicados não são tratadas como equivalentes, pois os
  protocolos experimentais diferem.

A apresentação foi compilada e verificada com 12 páginas.
