# 🎥 SAM 2 Video Segmentation Pipeline

Este projeto demonstra como configurar, carregar e utilizar o modelo **SAM 2 (Segment Anything Model)**, da Meta AI, para segmentação automática de objetos em vídeos com o auxílio de cliques manuais para anotação inicial.

## 📌 Objetivo

Aplicar o modelo SAM 2 para segmentar objetos em vídeos frame a frame com base em cliques positivos fornecidos manualmente. A pipeline inclui:
- Preparação do ambiente (Colab)
- Instalação das dependências
- Download e carregamento do checkpoint
- Extração dos frames do vídeo
- Inicialização e inferência com SAM 2
- Visualização dos resultados
- Exportação para vídeo final segmentado

---

## 🛠️ Tecnologias e Bibliotecas Utilizadas

- Python 3.10
- PyTorch 2.5.1
- Torchvision 0.20.1
- OpenCV
- Matplotlib
- SAM 2 (Facebook Research)
- ffmpeg (para extração de frames)
- Google Colab (ambiente de execução)

---

## ⚙️ Configuração do Ambiente

Certifique-se de estar usando o Google Colab com `using_colab = True`. O notebook realiza a instalação automática de todas as dependências necessárias:

```python
!pip install opencv-python matplotlib 'git+https://github.com/facebookresearch/sam2.git'
!wget -P ../checkpoints/ https://dl.fbaipublicfiles.com/segment_anything_2/092824/sam2.1_hiera_large.pt
