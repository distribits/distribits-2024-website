# Distribits meeting website sources

- The website is built with [hugo](https://gohugo.io/) and uses [a fork](https://github.com/distribits/hugo-PaperMod) of the [PaperMod](https://themes.gohugo.io/themes/hugo-papermod/) theme.
- Theme is attached as a submodule (supports dark & light mode)
- Content is written in Markdown and placed in `content/`
  - One file corresponds to one page;
    include `menu: "main"` and `weight: N` in front matter to determine placement in the top menu.
  - News items can be placed in `content/news/` folder, one file per news item;
    include `layout: post` and `date: yyyy-mm-dd` in front matter to determine placement in the News page.
- Home page (title, icons, social links) is generated based on configuration only
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
