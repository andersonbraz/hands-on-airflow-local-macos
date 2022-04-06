# HandsOn Aiflow Local on MacOS

Neste tutorial eu prefiro baixar/clonar diretamente o pyenv e definir minhas variáveis de ambiente para posteriormente instalar um AirFlow com a versão correta do Python.

## Step 1 - Download PyEnv

```shell
git clone https://github.com/pyenv/pyenv.git ~/.pyenv
```

## Step 2 - Set Variable

```shell
echo 'export PYENV_ROOT="$HOME/.pyenv"' >> ~/.zshrc
echo 'export PATH="$PYENV_ROOT/bin:$PATH"' >> ~/.zshrc
echo 'eval "$(pyenv init --path)"' >> ~/.zshrc
source ~/.zshrc
```

## Step 3 - Check Version PyEnv

```shell
pyenv --version
```

## Step 4 - Check Python in Use

```shell
python --version
```
ou

```shell
python3 --version
```

## Step 5 - Check Versions Installed on PyEnv

```shell
pyenv versions
```

## Step 6 - Check Versions Availble for PyEnv

```shell
pyenv install -l
```

## Step 7 - Installed Python Version 3.7.13 in  PyEnv

```shell
pyenv install 3.7.13
```

## Step 8 - Set ython Version 3.7.13 as Global (Default)

```shell
pyenv global 3.7.13
```

## Step 9 - Execute Script Install AirFlow

```shell
chmod +x install-airflow.sh && ./install-airflow.sh
```

## Step 11 - Check Version and Info AirFlow

```shell
airflow version && airflow info
```

## Step 11 - Init DB AirFlow

```shell
airflow db init
```

## Step 12 - Start AirFlow Standalone

```shell
airflow standalone
```

## Step 13 - Start AirFlow Standalone

```shell
airflow db init

airflow users create --username admin --firstname Anderson --lastname Braz --role Admin --email contato@andersonbraz.com

airflow webserver --port 8080

airflow scheduler
```
## IMPORTANT

[http://127.0.0.1:8080/home](http://127.0.0.1:8080/home)

## REFERENCES

[https://stackoverflow.com/questions/54965230/how-to-prevent-execution-failederrno-32-broken-pipe-in-airflow](https://stackoverflow.com/questions/54965230/how-to-prevent-execution-failederrno-32-broken-pipe-in-airflow)

[https://github.com/apache/airflow/blob/v1-10-stable/airflow/contrib/hooks/ssh_hook.py](https://github.com/apache/airflow/blob/v1-10-stable/airflow/contrib/hooks/ssh_hook.py)
