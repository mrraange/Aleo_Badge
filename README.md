# Aleo_Badge

1. Ставим необходимые пакеты

<code>apt install git</code>

<code>apt install curl</code>

<code>curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh</code>

<code>source "$HOME/.cargo/env"</code>

<code>sudo apt-get install wget gpg</code>

<code>wget -qO- https://packages.microsoft.com/keys/microsoft.asc | gpg --dearmor > packages.microsoft.gpg</code>

<code>sudo install -D -o root -g root -m 644 packages.microsoft.gpg /etc/apt/keyrings/packages.microsoft.gpg</code>

<code>sudo sh -c 'echo "deb [arch=amd64,arm64,armhf signed-by=/etc/apt/keyrings/packages.microsoft.gpg] https://packages.microsoft.com/repos/code stable main" > /etc/apt/sources.list.d/vscode.list'</code>

<code>rm -f packages.microsoft.gpg</code>

<code>sudo apt install apt-transport-https</code>

<code>sudo apt update</code>

<code>sudo apt install code</code>

<code>sudo apt install build-essential</code>

<code>apt install pkg-config</code>

<code>sudo apt-get update</code>

<code>sudo apt-get install libssl-dev</code>

2. Формируем ключ для подключения к Github

<code>ssh-keygen -t ed25519  -C "ВАШ ЕМЕЙЛ"</code>

<code>eval "$(ssh-agent -s)"</code>

<code>ssh-add ~/.ssh/id_ed25519</code>

<code>cat ~/.ssh/id_ed25519.pub</code>

строку вывода вставляем в Github  в настройки ssh

3. Установка leo и tictactoe

<code>git clone https://github.com/AleoHQ/leo </code>

<code>cd leo </code>

<code>cargo install --path . </code>

--Создаем кошелек

<code>leo account new</code>

Или вы можете импортировать свой текущий кошелек:

<code>leo account import your_private_key (вместо your_private_key - ваш приватник)</code>

<code>leo example tictactoe </code>

<code>cd tictactoe</code>

<code>leo run new </code>

<code>git init</code>

<code>git add .</code>

<code>git config --global user.email ВАШ ЕМЕЙЛ</code>

<code>git config --global user.name ВАШ ЮЗЕРНЕЙМ</code>

<code>git commit -m "My First commit"</code>

--идем в гитхаб и создаем репозиторий

--Обратно к терминалу

<code>git branch -m main</code>

<code>git remote add origin your_repository_link   (вместо your_repository_link - ссылка на ваш репозиторий)</code>

<code>git remote -v</code>

<code>git push -u origin main</code>

Перейдите в репозиторий [Leo](https://github.com/AleoHQ/leo/issues) и нажмите "New Issue" в справа 

Нажмите "Get started" в строке Leo Contributor Badge

В title вставьте: Add your_username to contributors (вместо your_username - ваш юзернейм в гитхабе)

В описании вставьте:

Hi Aleo team! I’m claiming my contributor badge for completing the New Developer Toolkit tutorial.

Github Username: ВАШ ЮЗЕРНЕЙМ

Tutorial Repo: your_repository_link (вместо your_repository_link - ссылка на ваш репозиторий)

Requested badge: Tutorial

Нажимаем "Submit New Issue"
