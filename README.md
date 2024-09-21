
# Install For WSL + DOCKER+ WEBUI:

```bash
wsl -d ubuntu
```
```bash
sudp apt update
sudo apt upgrade -y
curl -fsSL https://ollama.com/install.sh | sh
```

# to check resources de video
```bash
watch -n 0.5 nvidia-smi
```

# Install Docker
# Add Docker's official GPG key:

```bash
sudo apt-get update
sudo apt-get install ca-certificates curl
sudo install -m 0755 -d /etc/apt/keyrings
sudo curl -fsSL https://download.docker.com/linux/ubuntu/gpg -o /etc/apt/keyrings/docker.asc
sudo chmod a+r /etc/apt/keyrings/docker.asc
```


# Add the repository to Apt sources:
```bash
echo \
"deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/docker.asc] https://download.docker.com/linux/ubuntu \
$(. /etc/os-release && echo "$VERSION_CODENAME") stable" | \
sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
sudo apt-get update
```
```bash
sudo apt-get install docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin
```
```bash
sudo docker run -d --network=host -v open-webui:/app/backend/data -e OLLAMA_BASE_URL=http://127.0.0.1:11434 --name open-webui --restart always ghcr.io/open-webui/open-webui:main
```

# Check the docker
```bash
sudo docker ps
```


# Install Pyenv prereqs
```bash
sudo apt install -y make build-essential libssl-dev zlib1g-dev \
libbz2-dev libreadline-dev libsqlite3-dev wget curl llvm libncurses5-dev \
libncursesw5-dev xz-utils tk-dev libffi-dev liblzma-dev git
```


```bash


# Install Pyen
curl https://pyenv.run | bash
```

```bash
export PYENV_ROOT="$HOME/.pyenv"
[[ -d $PYENV_ROOT/bin ]] && export PATH="$PYENV_ROOT/bin:$PATH"
eval "$(pyenv init -)"
```


# refresh terminal
```bash
source .bashrc
```
```bash
#check if work pyenv
pyenv -h
```


# Install Python 3.10

```bash
pyenv install 3.10
pyenv global 3.10
```
# Install Stable Diffusion
```bash
wget -q https://github.com/ushio2580/apkis/blob/main/savadata/testing.sh
```

# Make it executable
```bash
chmod +x testing.sh
```


# Run it
```bash
./webui.sh --listen --api
```
# TORCHCHAT+PYTHORCH ~
```bash
git clone https://github.com/pytorch/torchchat.git
cd torchchat
python3 -m venv .venv
source .venv/bin/activate
./install/install_requirements.sh
```
```bash
python3 torchchat.py --help
```
# Download Model 
```bash
python3 torchchat.py download open-llama
```
# Testing Model
```bash
python3 torchchat.py generate open-llama --prompt "write me a story about a boy and his bear"
```
# Run Streamlit
```bash
streamlit run torchchat/usages/browser.py
```

# Install for 🔎💻影片 GPT script🔎💻
```bash
pip install streamlit langchain openai Wikipedia tiktoken
```
# Run Streamlit
```bash
streamlit run app.py
```

# Checking
```bash
python3 -m venv .venv
source .venv/bin/activate
```
