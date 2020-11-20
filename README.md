# Wowchemy Widget Starter Template

**Looking to build and publish a [Wowchemy](https://wowchemy.com) widget that doesn’t exist yet?**

_[**Wowchemy**](https://wowchemy.com) makes it easy to create a beautiful website for free. Edit your site in Markdown, Jupyter, or RStudio, generate it with Hugo, and deploy with GitHub or Netlify. Customize anything on your site with widgets, themes, and language packs._

## 👉 Core Concepts

- Each Wowchemy widget consists of an HTML file
- You may use [Go Templating](https://gohugo.io/templates/introduction/) and [Bootstrap](https://getbootstrap.com/docs/4.5/layout/grid/) layouts to design the widget HTML

## 🧑‍🎨 Create a Widget

1. Click the [_Use This Template_](https://github.com/wowchemy/wowchemy-widget-starter/generate) button on GitHub
   1. Name your repository `wowchemy-widget-<WIDGET-NAME>` where <WIDGET-NAME> is an appropriate name for your widget
1. Browse your new GitHub project, click the  `go.mod` file, and then the pencil button to edit it
   1. Replace the placeholder URL in `go.mod` with your new GitHub URL in the form `module github.com/<USERNAME>/wowchemy-widget-<WIDGET-NAME>` where `<USERNAME>` is your GitHub username and `<WIDGET-NAME>` is the name of the widget
1. Rename `my-widget.html` in the `layouts/partials/widgets/` folder to give it a unique ID in the form `github.<USERNAME>.<WIDGET-NAME>.html`, again replacing  `<USERNAME>` with your GitHub username and `<WIDGET-NAME>` with your widget name
1. Edit the HTML for your new widget
   - You may use [Go Templating](https://gohugo.io/templates/introduction/) and [Bootstrap](https://getbootstrap.com/docs/4.5/layout/grid/) layouts
   - You can access page and section (widget instance) variables using `$page` and `$section`, respectively
   - Check out the [built-in widgets](https://github.com/wowchemy/wowchemy-hugo-modules/tree/master/wowchemy/layouts/partials/widgets) for inspiration

## 🌈 Add the Widget to your Site

1. Install your widget in your site by referencing it at the bottom of your `config/_defaults/config.toml`:
   ```toml
   # At the bottom of your `config.toml` is a Module section:
   [module]

     # Your existing modules will appear here.

     # Add your widget's GitHub URL below.
     # Replace <USERNAME> and <WIDGET-NAME> with your GitHub username and widget name, respectively.
     [[module.imports]]
       path = "github.com/<USERNAME>/wowchemy-widget-<WIDGET-NAME>"
   ```
1. Create an instance of your widget in `home/`, for example let's create `home/my-widget.md`:
   ```markdown
   ---
   # Replace <USERNAME> and <WIDGET-NAME> with your GitHub username and widget name, respectively.
   widget: 'github.<USERNAME>.<WIDGET-NAME>'

   # This file represents a page section.
   headless: true

   # Order that this section appears on the page.
   weight: 1

   title: Hello
   ---

   Welcome to my new widget!
   ```

## 📢 Share your widget

Share your widget with the community on [Discord](https://discord.gg/z8wNYzb) and [Twitter]().
