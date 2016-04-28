# Skinning player

## Structure

* Use `eplayer-skin-component` class on every element which is interactable with user
* Use `eplayer-skin-fullsize` class on every element which should fill 100% of player area
* Use `eplayer-skin-background` if you want to draw element behind skin controls
* Use `eplayer-skin-foreground` if you want to draw element above skin controls

## Using common components

You can use some common classes in your skins and plugins to let player appearance be consistent.

* `eplayer-holdable` allows skin to automatically hide elements when neccessary
* `eplayer-skin-pane` draws pane according to player skin styles and colors
* `eplayer-skin-button` will draw button according coloring styles

## Using color styles

Usually using button and pane components is enough to build simple plugin or skin.

However you can use these styles to build more complex interface.

* `eplayer-text-color` will set color property to *text-color* color of player template
* `eplayer-text-color-background` will set background color property to *text-color* property of player template
* `eplayer-hover-color` will set color on hover elements to *hover-color* property of player template
* `eplayer-active-color` will set color property to *active-color* of player template 

## HAML templates for plugins

All haml files are compiled to player JS file. You can reference it by calling 

    $(window["eplayer-templates"][PATH])

Where PATH is a relative HAML path from src dir, for example `plugins/share_embed.html`

## Translations

You can use player translate API by passing HTML element code to translateElement function.

It will recursively translate all element and all of its sub-elements with translate="constant" property

Example HTML:

Example call:

    player.translateElement(this.$elm)


