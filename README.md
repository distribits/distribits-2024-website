# DataLad & git-annex meeting website (draft)

- The website is built with [hugo](https://gohugo.io/) and uses [PaperMod](https://themes.gohugo.io/themes/hugo-papermod/) theme.
- Content is written in Markdown and placed in `content/`
  - By default, a file corresponds to a page, listed in the menu
  - Blog posts can be placed in `content/posts/` folder
- Home page (title, icons, social links) is generated from configuration values
- Configuration is done with toml, in `config.toml`
- Theme is attached as a submodule (supports dark & light mode)
- There is a github action for deploying to GitHub pages, which builds to gh-pages branch
- As with any static generator, the content can be built locally and deployed anywhere

Local development & preview:

```
sudo apt install hugo
git clone --recurse-submodules <repo url>
cd meeting-website-draft
hugo server
```
