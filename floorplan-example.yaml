type: picture-elements
image: /local/floorplan/demo/NOME_FILE_NOTTE.png
style: |
  ha-card {
    border: none;
  }
elements:
  - type: image
    entity: sun.sun
    state_image:
      above_horizon: /local/floorplan/demo/NOME_FILE_GIORNO.png
      below_horizon: /local/floorplan/transparent.png
    style:
      height: 100%
      width: 100%
      left: 50%
      top: 50%
      mix-blend-mode: lighten
      opacity: 1
    action: none
    tap_action:
      action: none
    hold_action:
      action: none
# LUCI BIANCHE
  - type: image
    entity: light.entita_luce_bianca
    image: /local/floorplan/transparent.png
    style:
      pointer-events: none
      opacity: >-
        ${states['light.entita_luce_bianca'].state === 'on' ?
        (states['light.entita_luce_bianca'].attributes.brightness / 255) :0}
      mix-blend-mode: lighten
      transform: none
      top: 0%
      left: 0%
    state_image:
      'on': /local/floorplan/demo/NOME_FILE_LUCE_BIANCA.png
      'off': /local/floorplan/transparent.png
    tap_action:
      action: none
# LUCI COLORATE
  - type: custom:config-template-card
    entities:
      - light.entita_luce_colorata
    element:
      type: image
      image: /local/floorplan/demo/NOME_FILE_LUCE_BIANCA.png
      tap_action:
        action: none
      hold_action:
        action: none
    style:
      pointer-events: none
      opacity: >-
        ${ ( states["light.entita_luce_colorata"].attributes.brightness ?
        states["light.entita_luce_colorata"].attributes.brightness / 150 : 0) -
        (states["light.entita_luce_colorata"].attributes.hs_color ?
        states["light.entita_luce_colorata"].attributes.hs_color[1]/100 : 0)}
      mix-blend-mode: lighten
      top: 0%
      left: 0%
      transform: none
  - type: custom:config-template-card
    entities:
      - light.entita_luce_colorata
    element:
      type: image
      image: /local/floorplan/demo/NOME_FILE_LUCE_ROSSA.png
      tap_action:
        action: none
      hold_action:
        action: none
    style:
      pointer-events: none
      filter: >-
        ${ "sepia(100%)  hue-rotate(calc(" +
        (states['light.entita_luce_colorata'].attributes.hs_color ?
        states['light.entita_luce_colorata'].attributes.hs_color[0] : 0) + "deg
        - 55deg)) saturate(calc(" +
        (states['light.entita_luce_colorata'].attributes.hs_color ?
        states['light.entita_luce_colorata'].attributes.hs_color[1] : 100)+"%
        *4"}
      opacity: >-
        ${states['light.entita_luce_colorata'].state === 'on' ?
        (states['light.entita_luce_colorata'].attributes.brightness / 255) :0}
      mix-blend-mode: lighten
      top: 0%
      left: 0%
      transform: none
# BOTTONE
  - type: custom:button-card
    icon: mdi:lightbulb  #cancella questa riga se hai gia impostato l'icona nelle impostazioni dell'entità o senno scegli pure quella che piu ti piace
    color_type: icon
    tap_action:
      action: toggle
    hold_action:
      action: more-info
    entity: light.NOME_ENTITA'
    show_name: false
    show_icon: true
    show_label: false
    size: 70%
    styles:
      icon:
        - color: var(--button-card-light-color)
      card:
        - border-radius: 40%
        - width: 30px
        - background-color: rgba(255,255,255,0.1)
      label:
        - background-color: rgba(255,255,255,0.1)
    style:
      top: 50%
      left: 50%
