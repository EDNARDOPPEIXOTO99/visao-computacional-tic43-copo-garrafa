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
