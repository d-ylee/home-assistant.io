---
type: card
title: "Area card"
sidebar_label: Area
description: "The area card gives control of your entities in a specified area."
---

The area card lets you control and monitor an individual area.

<p class='img'>
  <img src='/images/dashboards/area-card.png' alt='Screenshot of the area card'>
  Screenshot of the area card.
</p>

{% include dashboard/edit_dashboard.md %}

All options for this card can be configured via the user interface.

Buttons will appear on the card for the entities in the area including fan, light and switch. A motion sensor icon will appear in the top left if a motion sensor is in the area and motion is detected by the motion sensor.

If a camera is added to the area you can show the camera feed instead of the area picture.

## YAML configuration

The following YAML options are available when you use YAML mode or just prefer to use YAML in the code editor in the UI.

{% configuration %}
type:
  required: true
  description: "`area`"
  type: string
area:
  required: true
  description: ID of the `area`.
  type: string
show_camera: 
  required: false
  description: Changes the area picture to a live feed of the camera set for the area.
  type: boolean
  default: false
navigation_path:
  required: false
  description: link to view. For more information about views, see the [view documentation](/dashboards/views/)
  type: string
theme:
  required: false
  description: Override the used theme for this card with any loaded theme. For more information about themes, see the [frontend documentation](/integrations/frontend/).
  type: string
{% endconfiguration %}

### Example

Basic example:

```yaml
type: area
area: bedroom
```

Complex example

```yaml
type: area
area: bedroom
navigation_path: my_bedroom
show_camera: true
theme: green
```
