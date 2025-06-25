# Transfer-Learning-Cats-Dogs
Projeto de Transfer Learning em Python.  O projeto consiste em aplicar o método de Transfer Learning em uma rede de Deep Learning na linguagem Python no ambiente COLAB.


# Transfer Learning para Classificação de Cães e Gatos

Este projeto demonstra o uso de Transfer Learning com a arquitetura MobileNetV2 para classificar imagens entre cães e gatos.

## Link do colab (somente leitura)
https://colab.research.google.com/drive/1dZh6X1cFzMwgUphO1a_4O0lukdZstTiK?usp=sharing

## Objetivos

*   Demonstrar o uso de Transfer Learning com MobileNetV2.
*   Construir um modelo capaz de classificar imagens de cães e gatos com alta acurácia.
*   Compartilhar o conhecimento adquirido.

## Dados

Este projeto utiliza um conjunto de dados de imagens de cães e gatos, organizado na seguinte estrutura de diretórios:


![image](https://github.com/user-attachments/assets/cc7008a8-41ad-4a7b-9a89-f9c5e4ef473f)


*   Número de imagens de gatos na pasta de treinamento: 401
*   Número de imagens de cachorros na pasta de treinamento: 401
*   Número de imagens de gatos na pasta de validação: 101
*   Número de imagens de cachorros na pasta de validação: 101
*   Fonte dos dados: As imagens de cães e gatos foram coletadas de diversas fontes na internet.

## Metodologia

Este projeto utiliza Transfer Learning com a rede pré-treinada MobileNetV2. Os dados foram pré-processados usando as seguintes técnicas:

*   Rescale: Os valores dos pixels foram redimensionados para o intervalo [0, 1].
*   Aumento de dados: As imagens foram aumentadas usando as seguintes transformações:
*   Rotação: Rotação aleatória de até 20 graus.
*   Deslocamento horizontal: Deslocamento horizontal aleatório de até 20% da largura da imagem.
*   Deslocamento vertical: Deslocamento vertical aleatório de até 20% da altura da imagem.
*   Cisalhamento: Cisalhamento aleatório com intensidade de até 20%.
*   Zoom: Zoom aleatório de até 20%.
*   Inversão horizontal: Inversão horizontal aleatória.

As seguintes camadas foram adicionadas à rede pré-treinada:

*   Global Average Pooling 2D
*   Dense (128 neurônios, função de ativação ReLU)
*   Dense (1 neurônio, função de ativação sigmoid)

O modelo foi treinado usando o otimizador Adam, a função de perda binary cross-entropy e a métrica de acurácia.

## Resultados

Os seguintes resultados foram obtidos durante o treinamento:

*   Acurácia no conjunto de treinamento: 0.9816
*   Acurácia no conjunto de validação: 0.9844
*   Perda no conjunto de treinamento: 0.0548
*   Perda no conjunto de validação: 0.0441

[Inserir gráfico das curvas de aprendizado, se disponível]

## Como Executar o Código

1.  Abra o notebook `Transfer_Learning_Gatos_Cachorros.ipynb` no Google Colab (colab.research.google.com).
2.  Execute a primeira célula do notebook para conectar o Colab ao seu Google Drive. Siga as instruções que aparecerão para autorizar o acesso.
3.  Localize a célula que define a variável `DATA_DIR` e altere o caminho para apontar para a pasta onde você armazenou as imagens de gatos e cachorros no seu Google Drive. O caminho deve ter o seguinte formato: `/content/drive/MyDrive/NomeDaSuaPasta`.
4.  Execute todas as células do notebook na ordem em que aparecem. Você pode fazer isso clicando no botão "Executar tudo" no menu "Ambiente de execução".

## Dependências

Para executar este projeto, você precisará das seguintes bibliotecas:

*   TensorFlow
*   Keras
*   Matplotlib
*   Pillow (Pode ser necessário para abrir alguns arquivos de imagem)

Você pode instalar essas bibliotecas usando o pip:

```bash
pip install tensorflow
pip install keras
pip install matplotlib
pip install Pillow

Licença
Este projeto é licenciado sob a MIT License.

Contato
[Rodrigo Rocha] - [vadan.2r@gmail.com]
