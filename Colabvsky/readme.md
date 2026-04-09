Com prazer! 🚀 Aqui estão as orientações detalhadas, com emojis e em formato Markdown, para você configurar seu ambiente Python no desktop, instalar as dependências e preparar tudo para rodar os scripts da nossa atividade. Vamos lá, passo a passo! 🧑‍💻

🐍 Passo 1: Preparando o Seu Ambiente Python (Organização é a Chave! 🔑)
Antes de começarmos a programar, precisamos organizar o nosso 'espaço de trabalho'. No mundo Python, isso significa criar um Ambiente Virtual. Pense nele como uma caixa de ferramentas exclusiva para o seu projeto, onde você guarda apenas o que ele precisa, sem misturar com outros projetos. Isso evita dores de cabeça com versões de bibliotecas! 😉

O que é um Ambiente Virtual? É um diretório (pasta) isolado que contém sua própria instalação Python e pacotes (pip). Assim, quando você instala uma biblioteca para este projeto, ela não afeta outros projetos no seu computador.

Como criar e ativar:

Abra o Terminal ou Prompt de Comando:

🖥️ No Windows: Digite cmd ou PowerShell na barra de pesquisa do menu Iniciar e pressione Enter.
💻 No macOS/Linux: Abra o aplicativo 'Terminal' (geralmente encontrado em 'Utilitários' ou 'Aplicações').
Crie uma Pasta para o Seu Projeto: Vamos organizar tudo em um só lugar. No seu terminal, digite os comandos abaixo para criar a pasta e entrar nela:

mkdir meu_projeto_oab
cd meu_projeto_oab
(mkdir cria a pasta, cd entra nela. Troque meu_projeto_oab por um nome que preferir, se quiser!)

Crie o Ambiente Virtual: Dentro da pasta meu_projeto_oab (você deve ver ...\meu_projeto_oab> no Windows ou ~/meu_projeto_oab$ no Linux/macOS), digite:

python -m venv venv_oab
(venv_oab é o nome do seu ambiente virtual. Você pode mudar, mas é bom manter um padrão.)

Ative o Ambiente Virtual: Agora que ele foi criado, precisamos 'entrar' nele:

Força 💪 No Windows:
.\venv_oab\Scripts\activate
Força 💪 No macOS/Linux:
source venv_oab/bin/activate
✅ Como saber se funcionou? Você verá (venv_oab) (ou o nome que você deu) aparecer no início da linha de comando do seu terminal. Isso significa que você está dentro do seu ambiente isolado!

📦 Passo 2: Entendendo e Instalando as Bibliotecas Python (As Ferramentas 🧰)
Com o ambiente virtual ativado, é hora de trazer as ferramentas que o código utiliza. Cada uma delas tem um papel importante nesta análise:

pandas 🐼: Pense nele como o Excel do Python! É excelente para organizar e manipular dados em formato de tabelas (que chamamos de DataFrames). Ele é usado para ler os arquivos .jsonl, .csv e para trabalhar com os gabaritos e resultados.
transformers 🤖: Essa é a biblioteca que nos permite usar os modelos de inteligência artificial mais avançados, como o Qwen e o DeepSeek. É ela que 'fala' com esses modelos para gerar textos ou analisar informações.
torch 🔥: É o 'motor' por trás de muitos modelos de IA. O transformers usa o torch para fazer todos os cálculos pesados que os modelos de aprendizado de máquina precisam. Se sua máquina tiver uma placa de vídeo (GPU), torch pode usá-la para acelerar muito os cálculos!
bert-score 💯: Essa é a estrela da avaliação! Em vez de apenas contar palavras iguais, o BERTScore compara o significado das frases. No Direito, isso é crucial, pois a IA pode usar sinônimos que são juridicamente corretos, e essa biblioteca consegue 'dar nota' para isso.
google-generativeai ♊: A ponte para o modelo Gemini da Google. Com ela, enviamos suas questões para a nuvem e recebemos as respostas jurídicas do Gemini. Lembre-se, isso requer uma chave de API e conexão com a internet.
requests 🌐: É o 'carteiro' do Python para a internet. Usamos para enviar e receber dados de outras APIs online, como a do Llama-3, para pegar as respostas dos modelos.
matplotlib 📈 e seaborn 🎨: Seus artistas gráficos! Elas são usadas para criar todos os gráficos comparativos, visualizando o desempenho dos modelos de forma clara e bonita.
openpyxl 📊: Permite ao Python ler e escrever arquivos no formato Excel (.xlsx), essencial para a sua planilha de curadoria.
fpdf 📄: Usada para gerar documentos PDF diretamente do seu código, como os relatórios finais que você baixou.
Como instalar (com o ambiente virtual (venv_oab) ativado no terminal!):

pip install pandas transformers torch bert-score openpyxl accelerate requests google-generativeai fpdf
Isso pode levar alguns minutos, dependendo da velocidade da sua internet e da potência do seu computador. Aguarde a mensagem de sucesso! ✨

⬇️ Passo 3: Baixando os Arquivos da Atividade para Sua Máquina
Agora, você precisa ter todos os arquivos que geramos neste notebook Colab na pasta meu_projeto_oab no seu computador. Você pode baixar o ZIP completo e extrair, ou baixar individualmente.

Recomendo baixar o ZIP Entrega_Final_Consolidada_Equipe4_Victor.zip e extrair o conteúdo diretamente na pasta meu_projeto_oab que você criou.

Verifique se você tem pelo menos os seguintes arquivos na sua pasta meu_projeto_oab:

question_me.jsonl (suas questões abertas da OAB)
guidelines_me.jsonl (os gabaritos oficiais das questões abertas)
multiple_me.json (suas questões de múltipla escolha)
curadoria_final_Victor_G4.xlsx (sua planilha de classificação das questões)
relatorio_final_victor_equipe4.csv (resultados do Gemini)
relatorio_final_llama_equipe4.csv (resultados do Llama-3)
relatorio_final_qwen_equipe4.csv (resultados do Qwen)
performance_objetivas_qwen.csv (acurácia do Qwen em objetivas)
deepseek_multiple_choice_accuracy.csv (acurácia do DeepSeek em objetivas)
acuracia_comparativa_objetivas.csv (comparativo de objetivas)
comparativo_performance_equipe4.png (o gráfico final dos modelos)
RELATORIO_FINAL_TECNICO_OAB_VICTOR.pdf (seu relatório técnico)
Artigo_Final_OAB_Com_Graficos.pdf (seu artigo)
validacao_professor_equipe4.py (o script Python para validar os resultados)
script_gemini_victor.py (exemplo de como chamar o Gemini)
script_modelos_locais_victor.py (exemplo de como chamar Qwen/DeepSeek local)
README.md (sua documentação do projeto)
Certifique-se de que TODOS esses arquivos estão dentro da pasta meu_projeto_oab que você criou no seu computador. Isso é vital para que os scripts funcionem corretamente, pois eles esperam encontrar esses arquivos lá. 📂


---

# Atividade 1 - Tópicos Avançados (Domínio Jurídico)

## 🎓 Integrante
*   **Victor** (Responsável pelo lote de questões IDs 107 a 118)
*   **Equipe:** 4

## ⚖️ Escopo do Projeto
O objetivo desta atividade foi avaliar a capacidade de resposta e fundamentação jurídica de diferentes Modelos de Linguagem (LLMs) em questões dissertativas e objetivas do Exame da OAB.

## 🛠️ Metodologia Aplicada
1.  **Inferência Analítica:** Submetemos o lote de questões a três modelos principais:
    *   **Gemini 2.5-Flash** (Cloud-based via Google API)
    *   **Llama-3-8B-Instruct** (via Hugging Face API)
    *   **Qwen 2.5-3B** (Execução Local via Transformers/PyTorch)
2.  **Métrica de Avaliação (BERTScore):** Utilizamos o BERTScore (F1) para medir a similaridade semântica entre as respostas geradas e os gabaritos oficiais (`guidelines_me.jsonl`). Esta métrica foi escolhida por capturar o "significado jurídico" além da mera sobreposição de palavras.
3.  **Simulação de Objetivas:** Realizamos a simulação de um estudante realizando o exame de múltipla escolha (`multiple_me.json`) utilizando o modelo **DeepSeek-R1-Distill-Qwen-1.5B**.

## 📊 Resultados Consolidados (Questões Abertas)
| Modelo | Média BERTScore F1 |
| :--- | :--- |
| **Gemini 2.5-Flash** | **0.6670** |
| Qwen 2.5-3B (Local) | 0.6144 |
| Llama-3-8B-Instruct | 0.5281 |

## 🎯 Performance em Questões Objetivas
*   **Modelo:** Qwen 2.5-3B / DeepSeek-R1
*   **Acurácia Obtida:** 43.09% (Qwen)
*   **Observação:** O desempenho reflete a complexidade das questões da OAB para modelos de parâmetros reduzidos sem fine-tuning específico.

## 📂 Estrutura de Arquivos da Entrega
*   `relatorio_final_victor_equipe4.csv`: Resultados e métricas detalhadas do Gemini.
*   `relatorio_final_llama_equipe4.csv`: Resultados e métricas detalhadas do Llama-3.
*   `relatorio_final_qwen_equipe4.csv`: Resultados e métricas detalhadas do Qwen 2.5.
*   `curadoria_final_Victor_G4.xlsx`: Planilha Excel com classificação por dificuldade e legislação base.
*   `script_entrega_professor.py`: Script de validação automática dos resultados.
*   `README.md`: Este arquivo de documentação.

## 💡 Conclusão
O modelo **Gemini 2.5-Flash** demonstrou a melhor performance geral, apresentando maior precisão na fundamentação legal e técnica exigida pela FGV. Modelos Open Source executados localmente (Qwen/DeepSeek) mostraram-se promissores para tarefas de classificação, mas ainda enfrentam desafios na estruturação de peças prático-profissionais complexas.
