# [Wowchemy Block Starter Template](https://github.com/wowchemy/wowchemy-block-starter)

**Looking to build and publish a [Wowchemy Block](https://wowchemy.com/blocks/) that doesn’t exist yet?**

_[**Wowchemy**](https://wowchemy.com) makes it easy to create a beautiful website for free. Edit your site in Markdown, Jupyter, or RStudio, generate it with Hugo, and deploy with GitHub or Netlify. Customize anything on your site with blocks, themes, and language packs._

## 👉 Core Concepts

- Each Wowchemy block consists of an HTML file
- You may use [Go Templating](https://gohugo.io/templates/introduction/) and [Bootstrap](https://getbootstrap.com/docs/4.5/layout/grid/) layouts to design the block HTML

## 🧑‍🎨 Create a Block

1. Click the [_Use This Template_](https://github.com/wowchemy/wowchemy-block-starter/generate) button on GitHub
   1. Name your repository with an appropriate name for your block collection, such as `alices-wowchemy-blocks`
1. Browse your new GitHub project, click the  `go.mod` file, and then the ✏️ pencil button to edit it
   1. Replace the placeholder URL in `go.mod` with your new GitHub URL in the form `module github.com/<USERNAME>/<COLLECTION-NAME>` where `<USERNAME>` is your GitHub username and `<COLLECTION-NAME>` is a name for your collection of blocks
   1. Scroll to the bottom and click _Commit Changes_ to save
1. Browse to the `blocks/` folder, click `my-block.html`, and click the ✏️ pencil button to edit it
   1. Rename `my-block.html` in the text box to a unique ID in the form `github.<USERNAME>.<BLOCK-NAME>.html`, again replacing  `<USERNAME>` with your GitHub username and `<BLOCK-NAME>` with your block name. It's important to provide this **globally unique block name**, otherwise another block can conflict with your block.
   1. Repeat the above step to rename the style file, `my-block.scss`
   1. Scroll to the bottom and click _Commit Changes_ to save
1. Edit the HTML for your new block
   - You may use [Go Templating](https://gohugo.io/templates/introduction/) and [Bootstrap](https://getbootstrap.com/docs/4.5/layout/grid/) layouts
   - You can access page and block (page section) variables using `$page` and `$block`, respectively
   - Check out the [built-in blocks](https://github.com/wowchemy/wowchemy-hugo-themes/tree/main/modules/wowchemy/layouts/partials/blocks) for inspiration

### Example

Say your GitHub username is `pikachu` and you wish to create a block named `pokemon`:

1. We click _Use This Template_ and enter `wowchemy-block-pokemon` as the project name
1. We replace the first line of `go.mod` with `module github.com/pikachu/wowchemy-block-pokemon`
1. We browse to the `blocks/` folder, and rename `my-block.html` to `github.pikachu.pokemon.html`
1. We rename rename `my-block.scss` to `github.pikachu.pokemon.scss`
1. We customize the HTML in `github.pikachu.pokemon.html` and the style in `github.pikachu.pokemon.scss`
1. We add the block to our site and share the block with the community following the guide below

## 🌈 Add the Block to your Site

1. Install the block by referencing it in your `config/_defaults/config.yaml`:
   ```yaml
   module:
     imports:
       # Your block's GitHub URL (replace <USERNAME> and <COLLECTION-NAME> with your GitHub username and block collection name)
       - path: github.com/<USERNAME>/wowchemy-block-<COLLECTION-NAME>
   ```
1. Create an instance of your block in `home/`, for example let's create `home/my-block.md`:
   ```markdown
   ---
   # Replace <USERNAME> and <BLOCK-NAME> with your GitHub username and block name, respectively.
   widget: 'github.<USERNAME>.<BLOCK-NAME>'

   # This file represents a page section.
   headless: true

   # Order that this section appears on the page.
   weight: 1

   title: Hello
   ---

   Welcome to my new block!
   ```

## 📢 Share your block

Add the [wowchemy-hugo-extension](https://github.com/topics/wowchemy-hugo-extension) tag to your block's GitHub repository to help other users find it.

Share your block with the community on [Discord](https://discord.gg/z8wNYzb) and [Twitter](https://twitter.com/intent/tweet?text=I%27m%20creating%20a%20beautiful%20website%20section%20using%20the%20free%20%E2%9D%A4%EF%B8%8F%2C%20open%20source%20%40wowchemy%20Website%20Builder%20for%20%40GoHugoIO%20by%20%40GeorgeCushen%20%E2%9C%A8%20Have%20some%20feedback%3F%20Please%20comment%20%F0%9F%A4%97&hashtags=MadeWithWowchemy&url=https://wowchemy.com/).
