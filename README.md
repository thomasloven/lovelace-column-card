column-card
===========

A lovelace card which contains other cards and display them as if they were not inside a card at all.

It'll make sense once I put up some example screenshots. Promise!

Example configuration
---------------------

```yaml
views:
  title: My view
  panel: true
  cards:
    - type: vertical-stack
      cards:
        - type: glance
          title: Header of the view
          entities:
            - ...
        - type: custom:column-card
          cards:
            - type: entities
              title: Card1
              entities:
                - ...
            - type: entities
              title: Card2
              entities:
                - ...
            - type: entities
              title: Card3
              entities:
                - ...
```
