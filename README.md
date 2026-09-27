# Visão Computacional — Atividade 1 (Copo x Garrafa)

Projeto desenvolvido para a capacitação **"Visão Computacional — Residência em TIC43"** (Ciclo C4, Curso Básico), promovida pelo **IRede**.

- **Unidade:** 1 | **Capítulo:** 1 | **Tarefa:** 2
- **Professores responsáveis:** Alyson Bezerra / Matheus Araújo
- **Aluno:** Ednardo Pinheiro Peixoto

## Objetivo

Explorar conceitos fundamentais de Processamento Digital de Imagens (PDI) a partir de um mini dataset próprio, com duas classes de objetos:

- **Classe A:** Copo
- **Classe B:** Garrafa

## Conteúdo do notebook

O notebook (`Atividade1_Ednardo.ipynb`) aborda:

- **Parte A — Resolução:** impacto visual e técnico de reduzir a resolução espacial das imagens (100%, 50%, 20%)
- **Parte B — Espaço de Cor:** comparação entre RGB, HSV e escala de cinza, incluindo análise isolada dos canais R, G e B
- **Parte C — Quantização:** efeito da redução de níveis de cinza por pixel (256, 64, 32, 2 níveis)
- **Parte D — Formato de Arquivo:** comparação entre JPEG (com compressão) e PNG (sem perdas)
- **Parte E — Estrutura do dataset:** organização final das imagens em pastas por classe

## Estrutura do repositório

```
dataset/
  classe_A_copo/
    copo1.jpg ... copo5.jpg
  classe_B_garrafa/
    garrafa1.jpg ... garrafa5.jpg
Atividade1_Ednardo.ipynb
README.md
```

## Sobre as imagens

Fotos autorais, capturadas com smartphone Motorola Edge 30 Neo, sem filtros ou embelezamento automático, variando iluminação (natural, artificial e sombra), ângulo e distância (entre 30 cm e 1 metro) entre as imagens de cada classe.

## Ferramentas utilizadas

- Google Colab
- Python (OpenCV, NumPy, Matplotlib)


Atividade 2 — Suavização, Remoção de Ruído e Detecção de Bordas

Pasta: atividade2-suavizacao-bordas/

Unidade: 2 | Capítulo: 1 | Tarefa: 1 Professor responsável: Rafael Carmo

Objetivo

Aplicar técnicas de filtragem espacial para suavização e remoção de ruído, e comparar diferentes operadores de detecção de bordas, utilizando o mesmo mini dataset (Copo x Garrafa) construído na Atividade 1.

Conteúdo do notebook
Parte 1 — Seleção das imagens: escolha de 2 imagens por classe com maior indício de degradação (ruído, granulação, compressão), com justificativa baseada em análise de nitidez (variância do Laplaciano)

Parte 2 — Filtros de suavização: Média (3×3, 5×5), Gaussiano (σ=1, σ=3) e Mediana (3×3, 5×5), com análise de variância dos níveis de cinza

Parte 3 — Detecção de bordas sem suavização prévia: operadores de Sobel, Prewitt (implementado manualmente) e Canny (com dois limiares), avaliando bordas falsas e sensibilidade a ruído

Parte 4 — Detecção de bordas após suavização: reaplicação dos detectores de borda após o filtro de suavização mais adequado, com comparação quantitativa e conclusão crítica

Ferramentas utilizadas
Google Colab
Python (OpenCV, NumPy, Matplotlib)


---

## Atividade 3 — Filtragem de Imagens e Análise de Ruído (Domínio da Frequência)

Pasta: [`atividade3-filtragem-frequencia/`](./atividade3-filtragem-frequencia)

**Unidade:** 2 | **Capítulo:** 1 | **Tarefa:** 3
**Professor responsável:** Rafael Carmo

### Objetivo

Aplicar técnicas de filtragem no domínio da frequência (Transformada de Fourier) e analisar o impacto de ruído artificial (Gaussiano e Sal e Pimenta) sobre o mesmo mini dataset (Copo x Garrafa) construído na Atividade 1.

### Conteúdo do notebook

- **Parte 1 — Seleção das imagens:** 1 imagem de cada classe, com resolução, formato e características apresentadas
- **Parte 2 — Inserção de ruído:** ruído Gaussiano (μ=0, σ=25) e ruído Sal e Pimenta (2% dos pixels), com análise do impacto visual e estatístico de cada um
- **Parte 3 — Filtro passa-baixa gaussiano (frequência):** aplicação via FFT com dois cutoffs diferentes, avaliando o trade-off entre remoção de ruído e perda de detalhes
- **Parte 4 — Filtro passa-alta (frequência):** realce de bordas e estruturas de alta frequência via FFT
- **Parte 5 — Comparação final:** tabela com variância medida em cada etapa do pipeline e conclusão crítica sobre qual ruído mais degrada a imagem e qual filtro é mais adequado para cada caso

### Ferramentas utilizadas

- Google Colab
- Python (OpenCV, NumPy, Matplotlib, FFT via NumPy)
