/*
Title: Adding Themes
Description: How to theme the gui
Sort: 2
*/

1. Create a themes directory
2. Get some themes from https://community.home-assistant.io/c/projects/themes NB: call the files themename.yaml
3. Add in configuration.yaml  
````yaml  
    # Enables the frontend
    frontend:
      themes: !include_dir_merge_named themes/

    input_select: !include input_select.yaml

    automation: !include automation.yaml
````
4. Create input_select.yaml
5. Add input selects 
````yaml
     hass_theme:
       name: HASS Themes
       options:
         - default
         - Midnight
         - Dark_Cyan
       initial: default
       icon: mdi:theme-light-dark
````
5. Add into automation.yaml
````yaml
      - id: hass_theme
        alias: hass_theme
        initial_state: 'on'
        trigger:
          - platform: state
            entity_id: input_select.hass_theme
        action:
          - service: frontend.set_theme
            data_template:
              name: "{{ states.input_select.hass_theme.state }}
````
6. Check-in config and if it passes reboot
