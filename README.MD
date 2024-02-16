# Stash Theme / CSS Switcher

## New version 2.0

The new version no longer requires custom served folders to load CSS from. All CSS is side loaded through an additional Javascript file.

## Information about plugin

Adds a button that shows a menu, allowing you to change CSS Themes and apply various CSS snippets for Stash App. The CSS isn't made by myself and in the CSS files authors where known are referenced.

Only the CSS of one theme can be applied at a time, and any amount of snippets can be applied.

Clicking on any radio/checkbox to apply the CSS, saves the CSS content of the Stylesheet in the browsers local storage, with an applied flag, eitehr true or false which allows the script upon page navigation and refresh to apply previously selected stylesheets

Under Change Order of Menu Bar, you can drag the elements to reorder the main menu and upon dropping it will generate the required CSS. It should work on touchscreens also, tested on Chrome IOS.

![Theme Plugin 1](https://github.com/elkorol/Stash-App-Theme-Switch-Plugin/blob/193f54fce3914991440027c4b98fd30aa9402d29/images/1.png)

![Theme Plugin 2](https://github.com/elkorol/Stash-App-Theme-Switch-Plugin/blob/193f54fce3914991440027c4b98fd30aa9402d29/images/2.png)

## Other Requirements

## Usage

1. Copy repository into Stash plugins folder.
2. Reload plugins from settings and enable

## Credit

The CSS code used is provided by [Stash Community Themes](https://docs.stashapp.cc/user-interface-ui/themes) and [Stash Community Custom CSS Snippets](https://docs.stashapp.cc/user-interface-ui/custom-css-snippets).

## Possible Upgrades

Perhaps in future can build a makeshift Tampermonkey Style User Manager to handle scripts internally within Stash. Just need to code a way the userscripts are added last and any requires in the metadata block load before scripts and tagering which urls to be active upon.
