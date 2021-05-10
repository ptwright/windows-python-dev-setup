# windows-python-dev-setup

### WSL2
* https://docs.microsoft.com/en-us/windows/wsl/install-win10
* Using **Debian**, Windows Terminal

### Pyenv
* install dependencies: 
```bash
$ sudo apt install -y make build-essential libssl-dev zlib1g-dev \
libbz2-dev libreadline-dev libsqlite3-dev wget curl llvm libncurses5-dev \
libncursesw5-dev xz-utils tk-dev libffi-dev liblzma-dev python-openssl
```
* install pyenv:
```bash
$ curl https://pyenv.run | bash
```
* configure ~/.profile (before any reference to ~/.bashrc if sourced)
```bash
export PYENV_ROOT="$HOME/.pyenv"
export PATH="$PYENV_ROOT/bin:$PATH"
eval "$(pyenv init --path)"
```
* configure ~/.bashrc
```bash
eval "$(pyenv init -)"
```
* using pyenv to install python
  * list available versions: 
  ```bash
  $ pyenv install --list
  ```
  * install
  ```bash
  $ pyenv install -v 3.x.x
  ```
  * list installed versions
  ```bash
  $ pyenv versions
  ```
  * set global version
  ```bash
  $ pyenv global 3.x.x
  ```
  * set local version (in project directory)
  ```bash
  $ pyenv local 3.x.x
  ```
 
### venv
* Creation of virtual environments
```bash
python -m venv /path/to/new/virtual/environment
```
### IDE
* [VSCode with remote-wsl extension](https://code.visualstudio.com/blogs/2019/09/03/wsl2)
