📘 Sobre o Projeto — comparar_arquivos.py

O script comparar_arquivos.py foi desenvolvido para comparar dois arquivos CSV e identificar registros divergentes entre eles, com base em uma coluna-chave definida pelo usuário.
Ele é especialmente útil em cenários de auditoria de dados, conciliação financeira e validação entre sistemas (por exemplo, para verificar se o conteúdo de um arquivo “principal” está sincronizado com outro gerado a partir de uma fonte secundária).

O programa:

Lê dois arquivos CSV com separadores diferentes.

Compara as linhas pela chave definida (ex: nuop).

Identifica registros exclusivos de cada arquivo.

Gera um relatório de divergências consolidado (divergencias.csv), indicando a origem de cada linha.

Além disso, o script trata erros comuns como:

Falta de colunas obrigatórias.

Arquivos não encontrados.

Problemas de leitura e gravação.

📄 README.md
# 🔍 Comparador de Arquivos CSV

Script em Python para comparar dois arquivos CSV e identificar divergências entre eles com base em uma coluna-chave.  
Ideal para auditorias, conciliações e verificações de consistência entre sistemas.

---

## 🚀 Funcionalidades
- Leitura de dois arquivos CSV com **separadores personalizados**.
- Comparação entre os arquivos pela **coluna-chave configurável**.
- Identificação de registros exclusivos em cada arquivo.
- Geração de um relatório `divergencias.csv` com todas as linhas divergentes.
- Indicação clara da origem de cada divergência (`Apenas no arquivo 1` ou `Apenas no arquivo 2`).

---

## ⚙️ Configuração
No início do script, edite as variáveis conforme o ambiente:

```python
# Caminhos dos arquivos de entrada
arquivo1_path = 'saida_book.csv'
arquivo2_path = 'principal.csv'

# Separadores específicos de cada arquivo
separador_arquivo1 = ','
separador_arquivo2 = ';'

# Coluna usada como chave de comparação
coluna_chave = 'nuop'

# Pasta e nome do arquivo de saída
pasta_saida = '.'
arquivo_saida = 'divergencias.csv'

▶️ Como usar

Coloque os arquivos CSV na mesma pasta do script.

Execute o script no terminal:

python comparar_arquivos.py


Após a execução, o arquivo divergencias.csv será gerado com as linhas que não coincidem entre os dois arquivos.

📊 Exemplo de Saída (divergencias.csv)
nuop	coluna1_x	coluna1_y	OrigemDivergencia
1001	valorA		Apenas no saida_book.csv
1056		valorB	Apenas no principal.csv
🧩 Dependências

Certifique-se de ter o Python 3.x instalado e a biblioteca pandas:

pip install pandas

⚠️ Possíveis Erros
Erro	Causa Provável	Solução
FileNotFoundError	Arquivo não encontrado	Verifique o nome e o caminho dos arquivos
KeyError: 'nuop'	Coluna-chave inexistente	Altere a variável coluna_chave para o nome correto
PermissionError	Arquivo de saída aberto em outro programa	Feche o arquivo antes de rodar o script novamente
🧠 Autor

Vinicius Costa de Paula
💼 Analista e desenvolvedor Python especializado em automação de processos e integração de dados.
📍 São Paulo - Brasil
📧 viniciuscostawj@gmail.com
