---
Title: Heatmiser Support
Description: How to add heatmiser neohub
Sort: 1
---
#### Adding a Heatmiser Neohub 
1. Create custom_components folder
2. From custom_componsnts clone the git repo  
```bash
    git submodule add https://github.com/RJ/heatmiser-neohub.py.git climate
```
3. Add to configuration.yaml  
```yaml
    climate:
      platform: heatmiser_neohub
      host: 192.168.13.94
      port: 4242
      debug: True
```
