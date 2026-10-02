# Tutorial de Realização das Atividades

Este documento apresenta o passo a passo para configurar o ambiente,
criar o repositório da disciplina e realizar as atividades das aulas.

## 1. Criando o repositório da disciplina

Primeiro, cada aluno deve criar um **repositório público no GitHub**
para a disciplina.

Ao criar o repositório:

-   Defina o repositório como **Public**;
-   Adicione um arquivo `README.md`;
-   Selecione o template de `.gitignore` para **Python**;
-   Não é necessário criar outras branches. As atividades serão enviadas
    diretamente para a branch `main`.

O repositório ficará responsável por armazenar todas as atividades
realizadas durante a monitoria.

A de organização é:

``` text
seu-repositorio/
├── Aula 01/
│   ├── Aula.ipynb
│   ├── .env.example
│   ├── requirements.txt
│   └── Main.py
├── Aula 02/
│   ├── Aula.ipynb
│   ├── .env.example
│   ├── requirements.txt
│   └── Main.py
└── README.md
```

A estrutura poderá ser repetida para cada nova aula e atividade.

------------------------------------------------------------------------

## 2. Instalando e configurando o Git/Python

Para trabalhar com o repositório no computador, será necessário instalar o **Git** e o **Python**. Também será necessário configurar o **Visual Studio Code (VS Code)** para trabalhar com Python.

### 2.1 Instalando o Git

Para trabalhar com o GitHub pelo computador, é necessário ter o **Git** instalado.

Baixe e instale o Git pelo site oficial:

https://git-scm.com/downloads

Durante a instalação, as opções padrão são suficientes para a utilização das atividades.

Após a instalação, abra o **Git Bash**, PowerShell ou Prompt de Comando e verifique se o Git foi instalado corretamente:

```bash
git --version
```

Se o comando retornar a versão instalada do Git, a instalação foi concluída corretamente.

---

### 2.2 Instalando o Python

Para realizar as atividades, utilizaremos a linguagem **Python**. Portanto, ela também precisa estar instalada no computador.

Baixe o Python pelo site oficial:

https://www.python.org/downloads/

Durante a instalação no Windows, é importante marcar a opção:

```text
Add Python to PATH
```

Essa opção permite executar o Python diretamente pelo terminal.

Após a instalação, abra um novo terminal e verifique se o Python foi instalado corretamente:

```bash
python --version
```

Caso o comando não funcione, tente:

```bash
py --version
```

Se um dos comandos retornar a versão instalada do Python, a instalação foi concluída corretamente.

------------------------------------------------------------------------

## 3. Configurando seu nome e e-mail no Git

Antes de realizar commits, configure seu nome e o e-mail que serão
utilizados pelo Git.

Execute:

``` bash
git config --global user.name "Seu Nome"
```

Depois:

``` bash
git config --global user.email "seu-email@example.com"
```

Recomenda-se utilizar o mesmo e-mail associado à sua conta do GitHub.

Para verificar as configurações:

``` bash
git config --global user.name
git config --global user.email
```

Essas configurações identificam o autor dos commits realizados na sua
máquina.

------------------------------------------------------------------------

## 4. Clonando o repositório na sua máquina

Depois de criar o repositório no GitHub, será necessário baixá-lo para o
computador utilizando `git clone`.

No GitHub, abra o seu repositório e copie a URL disponibilizada em
**Code \> HTTPS**.

No terminal, navegue até o local onde deseja armazenar o projeto e
execute:

``` bash
git clone https://github.com/SEU-USUARIO/SEU-REPOSITORIO.git
```

Substitua a URL pelo endereço do seu próprio repositório.

Depois, entre na pasta criada:

``` bash
cd SEU-REPOSITORIO
```

A partir desse momento, essa pasta será a cópia local do seu repositório
do GitHub.

------------------------------------------------------------------------

# 5. Preparando cada aula

Para cada aula e respectiva atividade, deverá ser criada uma pasta
dentro do seu repositório.

Por exemplo:

``` text
Aula 01
Aula 02
Aula 03
```

A numeração deve acompanhar a aula correspondente.

Dentro da pasta da aula, copie os arquivos pedidos abaixo disponibilizados no diretório
da disciplina:

``` text
Aula 01/
├── Aula.ipynb
├── .env.example
└── requirements.txt
```

Os nomes dos arquivos podem variar conforme a aula. Utilize os arquivos
fornecidos no diretório correspondente àquela aula.

------------------------------------------------------------------------

# 6. Escolhendo como realizar a atividade

A partir dos arquivos da aula, existem duas formas de realizar a
atividade.

## OPÇÃO A --- Mais simples

Esta é a forma recomendada para quem deseja seguir uma estrutura mais
direta para a entrega.

### 6.1 Configurar a chave da Groq

Crie uma key do Groq em:

https://console.groq.com/keys

Depois de gerar sua chave, crie o arquivo `.env` a partir do arquivo de
exemplo disponibilizado.

No Windows:

``` powershell
copy .env.example .env
```

No macOS ou Linux:

``` bash
cp .env.example .env
```

Abra o arquivo `.env` e informe sua chave:

``` dotenv
GROQ_API_KEY=sua_chave_da_groq_aqui
```

A chave da Groq é uma **chave de API**, e não uma URL.

O arquivo `.env` deve permanecer fora do versionamento. Nunca coloque
sua chave diretamente no código e nunca faça commit dela. Contando que
o gitignore já esteja configurado, você não deve se preocupar com isto

### 6.2 Baixar dependências

Clique com o botão direito na pasta da aula e selecione a opção "Open in integreted terminal" e baixe as dependências do projeto com o comando:

``` bash
pip install -r requirements.txt
```

### 6.3 Criar o `Main.py`

Dentro da pasta da aula, crie um arquivo chamado:

``` text
Main.py
```

A resolução de **todos os TODOs solicitados no notebook** deverá ser
colocada nesse arquivo.

Ao finalizar, o código deve executar normalmente, sem erros.

Caso alguma seção da atividade solicite uma explicação ou justificativa
sobre sua resposta, essa explicação pode ser adicionada diretamente no
código utilizando comentários:

``` python
# Explicação da minha resposta:
# ...
```

A estrutura final poderá ficar assim:

``` text
Aula 01/
├── Aula.ipynb
├── .env
├── requirements.txt
└── Main.py
```

------------------------------------------------------------------------

# 7. OPÇÃO B --- Seguir a estrutura indicada no README

Na segunda opção, a atividade deverá ser realizada seguindo o
procedimento apresentado abaixo.

Crie um ambiente virtual:

``` bash
python -m venv .venv
```

No Windows PowerShell:

``` powershell
.\.venv\Scripts\Activate.ps1
```

No Prompt de Comando:

``` bat
.venv\Scripts\activate.bat
```

No macOS ou Linux:

``` bash
source .venv/bin/activate
```

Com o ambiente virtual ativado, instale as dependências:

``` bash
python -m pip install -r requirements.txt
```

Em seguida, configure a chave da Groq no arquivo `.env`:

``` dotenv
GROQ_API_KEY=sua_chave_da_groq_aqui
```

Depois, abra o notebook da aula no VS Code ou no Jupyter e execute as
células em ordem.

A resolução da atividade deverá ser adicionada ao notebook, seguindo o
que foi solicitado no próprio README e no conteúdo da aula.

A estrutura poderá ficar semelhante a:

``` text
Aula 01/
├── Aula.ipynb
├── .env
├── requirements.txt
└── README.md
```

------------------------------------------------------------------------

# 8. Como rodar o projeto localmente

Depois de realizar a configuração da atividade, é importante executar o projeto localmente para verificar se tudo está funcionando corretamente antes de realizar o commit e enviar os arquivos para o GitHub.

Antes disso, certifique-se de que:

* O arquivo `.env` foi criado;
* A variável `GROQ_API_KEY` foi preenchida corretamente;
* As dependências do `requirements.txt` foram instaladas;
* Todos os TODOs foram resolvidos no `Main.py`.

## 8.1 OPÇÃO A — Executando o `Main.py`

Na Opção A, toda a resolução dos TODOs deve estar no arquivo `Main.py`.

Dentro da pasta da aula, execute:

```bash
python Main.py
```

A atividade somente deve ser enviada para o GitHub depois que o `Main.py` estiver funcionando corretamente.

---

## 8.2 OPÇÃO B — Executando o notebook

Na Opção B, a resolução é realizada diretamente no notebook (`.ipynb`).

Abra o arquivo `.ipynb` no **VS Code** ou no **Jupyter Notebook**.

Execute as células do notebook **em ordem**, começando pela primeira e seguindo até a última.

A atividade somente deve ser enviada para o GitHub depois que o notebook puder ser executado corretamente.

---

Se o projeto estiver configurado corretamente, o programa deverá ser executado sem apresentar erros.

Caso ocorra algum erro, verifique principalmente:

1. Se o ambiente está configurado corretamente;
2. Se as dependências foram instaladas;
3. Se o arquivo `.env` existe;
4. Se a `GROQ_API_KEY` foi preenchida corretamente;
5. Se a resolução dos TODOs foi implementada corretamente.

------------------------------------------------------------------------

# 9. Enviando a atividade para o GitHub

Depois de finalizar a atividade, abra o terminal dentro da pasta
principal "./" do seu repositório.

Primeiro, verifique quais arquivos foram modificados:

``` bash
git status
```

Depois, adicione os arquivos ao commit:

``` bash
git add .
```

Crie um commit indicando que a atividade foi finalizada:

``` bash
git commit -m "Finaliza atividade da Aula xx"
```

Por fim, envie as alterações para o GitHub:

``` bash
git push origin main
```

------------------------------------------------------------------------

## 10. Checklist antes da entrega

Antes de considerar a atividade concluída, verifique:

-   [ ] A pasta da aula foi criada dentro do repositório;
-   [ ] Os arquivos disponibilizados para a aula foram copiados;
-   [ ] O ambiente de desenvolvimento foi configurado;
-   [ ] As dependências do `requirements.txt` foram instaladas;
-   [ ] A chave da Groq foi configurada no `.env`;
-   [ ] O arquivo `.env` não está sendo enviado ao GitHub;
-   [ ] Todos os TODOs foram resolvidos;
-   [ ] As explicações solicitadas foram adicionadas;
-   [ ] O código/notebook foi executado e está funcionando corretamente;
-   [ ] Foi realizado um `git commit`;
-   [ ] Foi realizado um `git push origin main`;
-   [ ] A atividade pode ser visualizada no repositório do GitHub.