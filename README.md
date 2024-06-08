# Projeto

Primeiro projeto apresentado na displina de Inteligência Computacional em Saúde ministrada pelo professor [Andre Georghton Cardoso Pacheco](https://github.com/paaatcha).

## Base de dados

A base de dados utilizada nesse projeto corresponde a um questionário chamado [*Behavioral Risk Fator Surveillance System* (BRFSS)](https://www.cdc.gov/brfss/index.html) de 2015 realizado pelo CDC (*Central Disease Control*) disponível na plataforma [UCI *Machine Learning Repository*](https://archive.ics.uci.edu/) como [CDC *Diabetes Health Indicators*](https://archive.ics.uci.edu/dataset/891/cdc+diabetes+health+indicators). Os atributos presentes na base de dados são:

            
| Atrbiuto             | Descrição                                                                                                                                                        | Valores                       |
| :---                 |     :---                                                                                                                                                         | :---                          |
| Diabetes_binary      | você tem diabetes?                                                                                                                                               | Sim (1) ou não(0)             |
| HighBP               | você tem pressão alta?                                                                                                                                           | Sim (1) ou não(0)             |
| HighChol             | você tem colesterol alto?                                                                                                                                        | Sim (1) ou não(0)             |
| CholCheck            | você realizou exame de colesterol nos últimos cinco anos?                                                                                                        | Sim (1) ou não(0)             |
| BMI                  | qual seu índice de massa muscular?                                                                                                                               | Número inteiro                |
| Smoker               | você é fumante?                                                                                                                                                  | Sim (1) ou não(0)             |
| Stroke               | você já teve um AVC?                                                                                                                                             | Sim (1) ou não(0)             |
| HeartDiseaseorAttack | você tem doença coronariana (DCC) ou infarto do miocárdio?                                                                                                       | Sim (1) ou não(0)             |
| PhysActivity         | você praticou atividade física nos últimos 30 dias?                                                                                                              | Sim (1) ou não(0)             |
| Fruits               | você consume uma ou mais frutas por dia?                                                                                                                         | Sim (1) ou não(0)             |
| Veggies              | você consume uma ou mais verduras por dia?                                                                                                                       | Sim (1) ou não(0)             |
| HvyAlcoholConsump    | você consume grandes quantidades de álcool (homens adultos que bebem mais de 14 drinques por semana e mulheres adultas que bebem mais de 7 drinques por semana)? | Sim (1) ou não(0)             |
| AnyHealthcare        | você tem algum plano de saúde?                                                                                                                                   | Sim (1) ou não(0)             |
| NoDocbcCost          | houve algum momento nos últimos 12 meses em que você precisou consultar um médico, mas não pôde por causa do custo?                                              | Sim (1) ou não(0)             |
| GenHlth              | você diria que, em geral, o quão boa é a sua saúde?                                                                                                              | Escala de 1 à 5               |
| MentHlth             | sobre sua saúde mental, que inclui estresse, depressão e problemas emocionais, por quantos dias durante os últimos 30 dias sua saúde mental não foi boa?         | Escala de 0 à 30              |
| PhysHlth             | sobre sua saúde física, que inclui doenças e lesões físicas, por quantos dias durante os últimos 30 dias sua saúde física não foi boa?                           | Escala de 0 à 30              |
| DiffWalk             | você tem muita dificuldade para andar ou subir escadas?                                                                                                          | Sim (1) ou não(0)             |
| Sex                  | qual o seu sexo?                                                                                                                                                 | Feminino (0) ou masculino (1) |
| Age                  | qual a sua idade?                                                                                                                                                | Sim (1) ou não(0)             |
| Education            | qual o seu nível de escolaridade                                                                                                                                 | Escala de 1 à 6               |
| Income               | qual a sua renda familiar anual?                                                                                                                                 | Escala de 1 à 8               |
 
## Instalação

As instruções de instalação a seguir são apresentadas para o sistema operacional [Ubuntu](https://ubuntu.com/). Testado apenas no [Ubuntu 22.04](https://releases.ubuntu.com/jammy/).

### Ambiente virtual

O pacote `python3-venv` é necessário para criar ambientes virtuais Python. Ambientes virtuais são úteis para isolar projetos Python e suas dependências. Para instalá-lo no Ubuntu 22.04, execute o seguinte comando:

```bash
sudo apt-get install python3-venv
```

### Obtendo o projeto

Agora, vamos clonar um repositório Git e criar um ambiente virtual Python:

```bash
# Baixe o projeto
git clone https://github.com/intel-comp-saude-ufes/2024-1-P1-classificador-diabetes.git

# Entre na pasta do projeto
cd 2024-1-P1-classificador-diabetes/

# Crie um ambiente virtual com nome '.venv'
python3 -m venv .venv

# Ative o ambiente virtual
source .venv/bin/activate
```

Após ativar o ambiente virtual, seu terminal de comando deverá mostrar o nome do ambiente entre parênteses, indicando que você está trabalhando no ambiente virtual. Para ter certeza que o ambiente virtual está ativado, basta executar:

```bash
which python3
```

A saída do comando acima deve ser algo como `/caminho/ate/a/pasta/do/projeto/2024-1-P1-classificador-diabetes/.venv/bin/python3`. Caso você observe algo como `/usr/bin/python3`, significa que o ambiente virtual não foi criado ou ativado corretamente.

### Instalando as dependências

Agora que você está em um ambiente virtual, instale as dependências do projeto usando `pip`. Caso você não o tenha instalado em seu computador, basta executar:

```bash
sudo apt-get install python3-pip
```

Então, você pode prosseguir com a instalação das dependências do projeto:

```bash
pip3 install -r requirements.txt
```

Após concluir essas etapas, você terá um ambiente virtual Python configurado com as dependências do projeto instaladas. Você pode executar o código do projeto neste ambiente virtual e isso não afetará seu ambiente Python global. Lembre-se de ativar o ambiente virtual sempre que trabalhar neste projeto usando o comando `source .venv/bin/activate` e `deactivate` quando terminar executando deactivate.
