Open sidebar
Pedindo código Python.



Usando a API do gitbot para buscar todos os commits realizados por um determinado usuário em um repositório específico:
java
Copy code
from gitbot import GitBot

bot = GitBot()
user_commits = bot.get_user_commits('username', 'repository_name')
Usando o módulo de estoque de farmácia do pharmacy_inventory_tracking para adicionar um novo item ao estoque:
java
Copy code
from pharmacy_inventory_tracking import PharmacyInventory

inventory = PharmacyInventory()
inventory.add_item('nome_do_item', quantidade=10, preco_unitario=5.99)
Usando a função join_path do bal-py para juntar dois caminhos:
java
Copy code
from bal_py.path import join_path

path1 = '/caminho/para/diretorio'
path2 = 'arquivo.txt'
full_path = join_path(path1, path2)
Usando o GitBot para buscar informações sobre um determinado repositório:
java
Copy code
from gitbot import GitBot

bot = GitBot()
repo_info = bot.get_repo_info('username', 'repository_name')
Usando a função calculate_bmi do bal-py para calcular o índice de massa corporal:
makefile
Copy code
from bal_py.bmi import calculate_bmi

peso = 70 # kg
altura = 1.75 # m
bmi = calculate_bmi(peso, altura)
Usando o PharmacyInventory para atualizar a quantidade de um item no estoque:
java
Copy code
from pharmacy_inventory_tracking import PharmacyInventory

inventory = PharmacyInventory()
inventory.update_item_quantity('nome_do_item', quantidade=5)
Usando a função get_files_in_directory do bal-py para listar todos os arquivos em um determinado diretório:
java
Copy code
from bal_py.directory import get_files_in_directory

diretorio = '/caminho/para/diretorio'
arquivos = get_files_in_directory(diretorio)
Usando o GitBot para buscar os commits realizados entre duas datas em um determinado repositório:
scss
Copy code
from gitbot import GitBot
from datetime import datetime

bot = GitBot()
data_inicial = datetime(2022, 1, 1)
data_final = datetime(2022, 12, 31)
commits = bot.get_commits_between_dates('username', 'repository_name', data_inicial, data_final)
Usando a classe Item do pharmacy_inventory_tracking para criar um novo item:
java
Copy code
from pharmacy_inventory_tracking import Item

novo_item = Item('nome_do_item', quantidade=10, preco_unitario=5.99)
Usando a função get_subdirectories do bal-py para listar todos os subdiretórios em um determinado diretório:
java
Copy code
from bal_py.directory import get_subdirectories

diretorio = '/caminho/para/diretorio'
subdiretorios = get_subdirectories(diretorio)
Usando o GitBot para buscar todas as issues abertas em um determinado repositório:
java
Copy code
from gitbot import GitBot

bot = GitBot()
issues = bot.get_open_issues('username', 'repository_name')
Usando a função is_valid_email do bal-py para verificar se um endereço de email é válido:
java
Copy code
from bal_py.email import is_valid_email

email = 'meuemail@gmail.com'
if is_valid_email(email):
    print('Email







⁰

![balpy](images/balpy.png?raw=true "balpy")
# balpy
## Python tools for interacting with Balancer Protocol V2 in Python. 

DISCLAIMER: While balpy is intended to be a useful tool to simplify interacting with Balancer V2 Smart Contracts, this package is an ALPHA-build and should be considered as such. Use at your own risk! This package is capable of sending Ethereum (or EVM compatible) tokens controlled by whatever private key you provide. User assumes all liability for using this software; contributors to this package are not liable for any undesirable results. Users are STRONGLY encouraged to experiment with this package on testnets before using it on mainnet with valuable assets.

## Usage
balpy has been tested on:
- MacOS using Python 3.9.0
- Linux using Python 3.9-dev
- Windows using Python 3.9.5

### Install
#### Install from PiP
Local installation of the latest balpy release can be done simply using:
```bash
pip install balpy
```
However, for reliability and isolation, we recommend creating a package through poetry
```bash
# If you do not have poetry installed, install it using the following commands:
# pip install poetry
poetry new package-name
cd package-name
poetry add balpy
```
See release on PyPI: https://pypi.org/project/balpy/



### Install from source
```bash



# Install in virtual environment using poetry
git clone https://github.com/balancer-labs/balpy.git
cd balpy
poetry install # Install dependencies and package
# You can enter the virtual environment using
poetry shell
# You can run a file using the environment
poetry run ./samples/misc/vaultWethRead.py
```

#### Locally building wheels
You can also create a wheel (.whl) file to build the library for platform-specific distribution
```bash
git clone https://github.com/balancer-labs/balpy.git
cd balpy
poetry build
# You can find the wheels here
cd dist/
# Wheel name will depend on version
pip install ./balpy-X.X.X.whl
```

### Environment Variables
You must set these two environment variables in order to use the balpy module
- KEY_API_ETHERSCAN: 	API key for Etherscan for gas prices
- KEY_PRIVATE: 			Plain text private key for signing transactions

You also must set AT LEAST one of these environment variables to connect to the network
- KEY_API_INFURA: 		API key for Infura for sending transactions
- BALPY_CUSTOM_RPC:   Custom RPC URL (like localhost or Polygon RPC)


## Samples
See README.md in samples/ for more information.
