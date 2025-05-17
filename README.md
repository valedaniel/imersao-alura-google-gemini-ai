# 🤖 Sistema de Criação de Posts para Instagram com IA Generativa

> Crie conteúdo para suas redes sociais de forma inteligente e automatizada!

## 📋 Sobre o Projeto

Este projeto implementa um sistema avançado de agentes de IA que trabalham em conjunto para criar posts de qualidade para Instagram sobre tópicos de interesse. Utilizando a API do Google Gemini e o framework ADK (Agent Development Kit), o sistema envolve quatro agentes especializados que atuam em uma pipeline coordenada.

## ✨ Funcionalidades

- 🔍 **Busca automática** de notícias e lançamentos recentes sobre o tópico escolhido
- 📝 **Planejamento estratégico** dos pontos mais relevantes para um post engajador
- ✏️ **Redação criativa** de rascunhos com linguagem adequada para redes sociais
- 🧐 **Revisão profissional** do conteúdo para garantir qualidade e adequação ao público-alvo

## 🛠️ Tecnologias Utilizadas

- **Google Gemini 2.0 Flash**: LLM avançado para processamento de linguagem natural
- **Google ADK (Agent Development Kit)**: Framework para desenvolvimento de agentes de IA
- **Google Search API**: Acesso a informações atualizadas da web para contextualização
- **Python**: Linguagem de programação principal
- **Google Colab**: Ambiente de desenvolvimento e execução

## 🏗️ Arquitetura do Sistema

O sistema é composto por 4 agentes especializados:

### 1. Agente Buscador
- **Função**: Pesquisa os lançamentos e notícias mais recentes sobre o tópico escolhido
- **Ferramentas**: Google Search API
- **Saída**: Lista de até 5 lançamentos relevantes e recentes sobre o tópico

### 2. Agente Planejador
- **Função**: Analisa os lançamentos encontrados e planeja o conteúdo do post
- **Ferramentas**: Google Search API
- **Saída**: Tema escolhido, pontos relevantes e estrutura do post

### 3. Agente Redator
- **Função**: Cria o rascunho do post com base no plano desenvolvido
- **Ferramentas**: Google Search API
- **Saída**: Rascunho de post para Instagram com linguagem engajadora

### 4. Agente Revisor
- **Função**: Revisa o conteúdo para qualidade, tom e adequação ao público
- **Ferramentas**: Google Search API
- **Saída**: Feedback ou versão revisada do post

## 🚀 Como Utilizar

### Pré-requisitos
- Conta no Google Colab
- Chave de API do Google Gemini
- Biblioteca google-genai e google-adk instaladas

### Configuração
1. Clone este repositório:
```bash
git clone https://github.com/seu-usuario/sistema-agentes-post-instagram.git
```

2. Abra o notebook `Imersão_IA_Alura_+_Google_Gemini_Aula_05_Agentes.ipynb` no Google Colab

3. Configure sua chave de API do Google Gemini:
```python
# No Google Colab, vá em "Secrets" e adicione:
# GOOGLE_API_KEY = "sua-chave-api-aqui"

import os
from google.colab import userdata
os.environ["GOOGLE_API_KEY"] = userdata.get('GOOGLE_API_KEY')
```

4. Instale as dependências:
```python
%pip install -q google-genai google-adk
```

5. Execute o notebook e siga as instruções para gerar seu post

## 📊 Exemplo de Uso

```python
# Execução do pipeline completo
topico = "NASA Astronomia"  # Insira o tópico de interesse

# 1. Buscar lançamentos recentes
lancamentos_buscados = agente_buscador(topico, data_de_hoje)

# 2. Planejar o conteúdo
plano_de_post = agente_planejador(topico, lancamentos_buscados)

# 3. Redigir o post
rascunho_gerado = agente_redator(topico, plano_de_post)

# 4. Revisar o conteúdo
texto_revisado = agente_revisor(topico, rascunho_gerado)

# O resultado final é um post pronto para ser publicado no Instagram!
```

## 📢 Resultados

O sistema gera posts de Instagram engajadores e informativos sobre tópicos de tecnologia, ciência ou qualquer área de interesse. Exemplo de saída para o tópico "NASA Astronomia":

> 🔭🌌 **IMAGEM:** Uma foto deslumbrante da galáxia M83 capturada pelo James Webb.
> 
> 💥 Preparados para essa? O Telescópio Espacial James Webb acaba de revelar um segredo cósmico na galáxia M83: um buraco negro supermassivo!
> 
> Localizada a 15 milhões de anos-luz, a M83 (ou Galáxia do Cata-Vento do Sul) escondia um Núcleo Galáctico Ativo (AGN). O JWST detectou emissões de gás neon ionizado, mostrando que um buraco negro gigante está se alimentando ali! 🕳️✨
> 
> Por que isso é tão incrível? 🤔 Entender esses "monstros cósmicos" nos ajuda a descobrir como as galáxias e o universo evoluem! Com sua visão infravermelha superpoderosa, o JWST consegue enxergar através da poeira cósmica e revelar segredos como esse.
> 
> O que acharam dessa descoberta? Comentem aqui embaixo e marquem um amigo que curte astronomia! 👇
> 
> #JWST #BuracoNegro #Astronomia #M83 #JamesWebbTelescope #Alura

## 🔄 Limitações e Possíveis Melhorias

- **Imagens**: Atualmente o sistema não gera imagens para os posts. Uma possível melhoria seria integrar APIs de geração de imagens como DALL-E ou Midjourney.
- **Personalização**: Adicionar opções para diferentes tons de voz e estilos de escrita.
- **Multi-plataforma**: Expandir para gerar conteúdo adaptado para outras redes sociais como Twitter, LinkedIn, etc.
- **Analytics**: Implementar avaliação da qualidade e potencial de engajamento dos posts gerados.

## 🙏 Agradecimentos

- [Alura](https://www.alura.com.br) e [Google](https://www.google.com) pela Imersão IA que inspirou este projeto
- Comunidade de desenvolvedores do Google Gemini e ADK

---

Desenvolvido com 💙 como parte da Imersão IA - Alura + Google Gemini
