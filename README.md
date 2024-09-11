# Fractal

tek seferde hepsi
  
    sudo apt-get update
    sudo apt-get install ca-certificates curl
    sudo install -m 0755 -d /etc/apt/keyrings
    sudo curl -fsSL https://download.docker.com/linux/ubuntu/gpg -o /etc/apt/keyrings/docker.asc
    sudo chmod a+r /etc/apt/keyrings/docker.asc
    
    # Add the repository to Apt sources:
    echo \
      "deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/docker.asc] https://download.docker.com/linux/ubuntu \
      $(. /etc/os-release && echo "$VERSION_CODENAME") stable" | \
      sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
    sudo apt-get update

tek tek sıradakiler

  
    sudo apt-get install docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin
  
    curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.40.0/install.sh | bash
    
    export NVM_DIR="$HOME/.nvm"
    [ -s "$NVM_DIR/nvm.sh" ] && \. "$NVM_DIR/nvm.sh"  # This loads nvm
    [ -s "$NVM_DIR/bash_completion" ] && \. "$NVM_DIR/bash_completion"
    
    nvm install 20
    
    node -v 
    
    npm -v 
    
    npm install -g yarn
    
    git clone https://github.com/CATProtocol/cat-token-box.git
    
    cd cat-token-box
    
    yarn install
    
    yarn build
    
    cd packages/tracker
    
    mkdir -p docker/data
    
    mkdir -p docker/pgdata
    
    sudo chmod 777 docker/data
    
    sudo chmod 777 docker/pgdata
    
    yarn install
    
    yarn build
    
    docker compose up -d
    
    cd ../../ && docker build -t tracker:latest .
    
    docker run -d \
        --name tracker \
        --add-host="host.docker.internal:host-gateway" \
        -e DATABASE_HOST="host.docker.internal" \
        -e RPC_HOST="host.docker.internal" \
        -p 3000:3000 \
        tracker:latest
    
    cd packages/cli
    
    yarn install
    
    yarn build
    
    
    while true; do    yarn cli mint -i 45ee725c2c5993b3e4d308842d87e973bf1951f5f7a804b21e4dd964ecd12d6b_0 5 --fee-rate "istediğiniz fee rate";   sleep 3; done

