# column-card

A lovelace card which contains other cards and display them as if they were not inside a card at all.

## Why?

Lovelace automatically puts your cards in nice columns, the number of which are determined by the screen width:
![example-original](https://user-images.githubusercontent.com/1299821/43414537-552140c4-9433-11e8-802c-640193b1cd12.png)

A known trick to get a header bar to a view is to make the view a panel, and add the header via a `vertial-stacḱ` card. But then you lose the columns. The best you can get is a `horizontal-stack`, but that doesn't adjust to the screen width.

Enter `column-card`. A card which takes other cards and display them in columns:
![example-after](https://user-images.githubusercontent.com/1299821/43414653-b9276cd8-9433-11e8-8c66-33002aee3561.png)

## Options

| Name | Type | Default | Description
| ---- | ---- | ------- | -----------
| type | string | **Required** | `custom:column-card`
| cards | list | **Required** | List of cards

## Instalation

1. Copy `column-card.js` to `<config directory>/www/column-card.js`
2. Add `column-card` as a resource in `ui-lovelace.yaml`

```yaml
resources:
  - url: /local/column-card.js
    type: js
```


## Example configuration

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
