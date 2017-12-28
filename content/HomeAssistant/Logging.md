---
Title: Add Logging Level Selector
Description: Hot to add a drop down to choose logging level
Sort: 3
---
1. Add to input_select.yaml
````yaml
    log_level:
      name: Log Level
      options:
        - critical
        - fatal
        - error
        - warning
        - warn
        - info
        - debug
        - notset
      initial: warn
````
2. Add to automations.yaml
````yaml
    - alias: Log Level
      trigger:
        platform: state
        entity_id: input_select.log_level
      action:
        service: logger.set_level
        data_template:
          homeassistant.components: "{{ trigger.to_state.state }}"
````