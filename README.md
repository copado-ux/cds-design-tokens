# CDS

# Figma Tokens

**Figma Tokens** is a [Figma Plugin](https://jansix.at/resources/figma-tokens) allowing you to integrate Tokens into your Figma designs.

It gives you reusable tokens that can be used for a whole range of design options, from border radii or spacer units to semantic color and typography styles. It allows you to change tokens and see these changes applied to the whole document or its styles.

## Design Tokens

*Design tokens are the visual design atoms of the design system — specifically, they are named entities that store visual design attributes. We use them in place of hard-coded values (such as hex values for color or pixel values for spacing) in order to maintain a scalable and consistent visual system for UI development. [Salesforce, Lightning Design System](https://www.lightningdesignsystem.com/design-tokens/)*

## Standard

The [W3C Design Tokens Community Group](https://github.com/design-tokens/community-group)
 aims to establish a standard on which tools can rely on for sharing design tokens. This plugin aims to be W3C compliant so you could take your JSON and move to another tool someday.

# GitHub Repo

Storing tokens on GitHub makes a lot of sense. It's version controlled, allows you to work in different branches (think of a brand refresh that lives on a different branch than the current live version) and gives you varying access levels such as Read or Write access. Also you can integrate GitHub Actions which will allow you to create a token pipeline with Style Dictionary or other tools.

[https://docs.tokens.studio/sync/github](https://docs.tokens.studio/sync/github)

# Tokens Pipeline - TBD

## Figma Tokens JSON

Figma tokens plugin generates a JSON file (data/tokens.json). This is the raw source of truth used for syncing the plugin. **This file cannot be used in development.** No math and aliases are resolved.

*NB This file can technically be manually edited and then the plugin can pull changes from the repo. However, to avoid mistakes, this file should be generated, as best practice, only by the Figma Tokens Plugin within the Figma enviroment.*

## Token Transformer

[Token Transformer](https://www.npmjs.com/package/token-transformer)
Converts tokens from Figma Tokens to something Style Dictionary can read, removing any math operations or aliases, only resulting in raw values.


## Sytle Dictionary

[Style Dictionary](https://github.com/amzn/style-dictionary)
A Style Dictionary uses design tokens to define styles once and use those styles on any platform or language. 

