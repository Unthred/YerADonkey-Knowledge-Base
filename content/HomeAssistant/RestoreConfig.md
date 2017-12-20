---
Title: New Home Assistant Machine
Description: How to restore home assistant to a new machine from github
Sort: 0
---
#### Configure Github

1. git init
2. Copy and paste the following (end by typing EOF & hit return)  
```bash
    cat <<EOF > .gitignore  
    *  
    !*.yaml 
    !scenes 
    !.gitignore  
    secrets.yaml  
    known_devices.yaml```
3. git remote add origin https://github.com/Unthred/Home-AssistantConfig.git
4. git fetch origin
5. git checkout -f -b master --track origin/master