# Stash Theme / CSS Switcher

Adds a button that shows a menu, allowing you to change CSS Themes and apply various CSS snippets for Stash App. The CSS isn't made by myself and in the CSS files authors where known are referenced.

Only the CSS of one theme can be applied at a time, and any amount of snippets can be applied.

Clicking on any radio/checkbox to apply the CSS, saves the CSS content of the Stylesheet in the browsers local storage, with an applied flag, eitehr true or false which allows the script upon page navigation and refresh to apply previously selected stylesheets

Under Change Order of Menu Bar, you can drag the elements to reorder the main menu and upon dropping it will generate the required CSS. It should work on touchscreens also, tested on Chrome IOS.

## Other Requirements

This plugin requires the feature of Stash - Custom Served Folders, to serve the stylesheets to stash. More here > [Advanced Configuration Options](https://github.com/stashapp/stash/wiki/Advanced-Configuration-Options), and here, [Add custom served folders](https://github.com/stashapp/stash/pull/620)

It perhaps could have been done by referencing the CSS in the yml file but I couldn't figure out how to add more than one without them merging.

## Usage

1. Copy repository into Stash plugins folder.
2. Stop Stash from running and find and open config.yml
3. Enter or add the relevent parts below, into config.yml

```yaml
custom_served_folders:
  /themeswitch: [Path to where you copied the repository plugin]\assets
```

*I.E.*

```yaml
custom_served_folders:
  /themeswitch: C:\Stash\plugins\theme_switch\assets
```

4. Open theme.js and edit STASHURL variable at the top to suit your configuration. If leaving it as localhost and accessing Stash on a third party device on your network via IP address, it will not work unless you set the variable to that IP address or if you have a custom domain/host setup
5. Start Stash, navigate to Settings > Plugins > Press Reload Plugins and refresh
6. The Theme / CSS Switcher button should now be in the top right of the menu bar

## Credit

The CSS code used is provided by [Stash Community Themes](https://docs.stashapp.cc/user-interface-ui/themes) and [Stash Community Custom CSS Snippets](https://docs.stashapp.cc/user-interface-ui/custom-css-snippets).

## Possible Upgrades

Perhaps in future can build a makeshift Tampermonkey Style User Manager to handle scripts internally within Stash. Just need to code a way the userscripts are added last and any requires in the metadata block load before scripts and tagering which urls to be active upon.
