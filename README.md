# Distribits meeting website sources

- The website is built with [hugo](https://gohugo.io/) and uses [a fork](https://github.com/distribits/hugo-PaperMod) of the [PaperMod](https://themes.gohugo.io/themes/hugo-papermod/) theme.
- Theme is attached as a submodule (supports dark & light mode)
- Content is written in Markdown and placed in `content/`
  - By default, a file corresponds to a page, listed in the menu
  - Blog posts can be placed in `content/posts/` folder
- Home page (title, icons, social links) is generated from configuration values
- Configuration is done with toml, in `config.toml`
- There is a github action for deploying to GitHub pages, which builds to gh-pages branch, which is deployed to the custom domain distribits.live
- As with any static generator, the content can be built locally and deployed anywhere

### Local development & preview:

```
sudo apt install hugo
git clone --recurse-submodules <repo url>
cd distribits-2024-website
hugo server
```

### Note about the index page

The `CALL FOR PARTICIPATION` section on the index page is a custom change
to the `layouts/partials/index_profile.html` file in the submodule located
at `themes/PaperMod2`. For a change to this section to reflect on the live website:
1. update the `layouts/partials/index_profile.html` page in the submodule
2. commit and push the changes to the fork's `master` branch at https://github.com/distribits/hugo-PaperMod
3. commit and push the submodule update (`themes/PaperMod2`) to the repo's `main` branch at https://github.com/distribits/distribits-2024-website