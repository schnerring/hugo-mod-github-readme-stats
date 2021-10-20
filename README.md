# hugo-mod-github-readme-stats

A Hugo module that thinly wraps the [GitHub Readme Stats project](https://github.com/anuraghazra/github-readme-stats).

GitHub Readme Stats works with Hugo out of the box. However, with this module,
you can also use them within your Hugo templates. Shortcodes are also included,
so you don't have to directly deal with query string parameters.

## Getting Started

Initialize your Hugo site as a Hugo module:

```shell
hugo mod init example.com
```

Add the following to the `config.toml` file of your site to import the module:

```toml
[module]
  [[module.imports]]
    path = "github.com/schnerring/hugo-mod-github-readme-stats"
```

Install the module:

```shell
hugo mod get
```
