# Skinning player

## Adding custom HTML and CSS

In most cases it is suitable to create custom CSS.

If you need more complex changes involving structure you can also build your own HTML.

To connect your assets to skins add parameters to player data with css and html paths. It could be URL or relative path.

## Structure

* Use `eplayer-skin-component` class on every element which is interactable with user
* Use `eplayer-skin-fullsize` class on every element which should fill 100% of player area
* Use `eplayer-skin-background` if you want to draw element behind skin controls
* Use `eplayer-skin-foreground` if you want to draw element above skin controls
* Use `eplayer-skin-shiftable` if you want to let background elements be shiftable by skin controls

## Using common components

You can use some common classes in your skins and plugins to let player appearance be consistent.

* `eplayer-holdable` allows skin to automatically hide elements when neccessary
* `eplayer-skin-pane` draws pane according to player skin styles and colors
* `eplayer-skin-button` will draw button according coloring styles

## Using color styles

Usually using button and pane components is enough to build simple plugin or skin.

However you can use these styles to build more complex interface.

* `eplayer-main-color` will set color property to *foreground-color* color of player template
* `eplayer-main-color-background` will set background color property to *foreground-color* property of player template
* `eplayer-text-color` will set color property to *text-color* color of player template
* `eplayer-text-color-background` will set background color property to *text-color* property of player template
* `eplayer-hover-color` will set color on hover elements to *hover-color* property of player template
* `eplayer-active-color` will set color property to *active-color* of player template 

## Responsible layout

* `eplayer-xs-hidden` will hide the element if player width is smaller then 400 px

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


