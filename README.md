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


Problems
--------
The columns are supposed to readjust automatically when the window has been resized.
While this does work, it's rather slow. It can take several seconds before the update happens.

If you know more about javascript than me (i.e. anything at all, really) and think you can fix this; please help!
