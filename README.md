# hugo-mod-github-readme-stats

A Hugo module that thinly wraps the [GitHub Readme Stats](https://github.com/anuraghazra/github-readme-stats)
project.

GitHub Readme Stats works with Hugo out of the box. However, with this module,
you can also use them within your Hugo templates. The module includes shortcodes,
so you don't have to deal with query string parameters.

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

## Configuration

Only the `class` parameter is specific to the module. If set, a `class`
attribute gets added to stat card `img` element.

For the rest of the configuration options, refer to the GitHub Readme Stats repo,
since the module only wraps the original config options:

- [Common Options](https://github.com/anuraghazra/github-readme-stats#common-options)
- [Stats Card Exclusive Options](https://github.com/anuraghazra/github-readme-stats#stats-card-exclusive-options)
- [Repo Card Exclusive Options](https://github.com/anuraghazra/github-readme-stats#repo-card-exclusive-options)
- [Language Card Exclusive Options](https://github.com/anuraghazra/github-readme-stats#language-card-exclusive-options)
- [Wakatime Card Exclusive Options](https://github.com/anuraghazra/github-readme-stats#wakatime-card-exclusive-options)

## Examples

You can use partials in your templates:

<!-- markdownlint-disable MD013 -->

```go-template
{{ partial "github-readme-stats/pin.html" (dict "username" "schnerring" "repo" "hugo-mod-github-readme-stats" "show_owner" "true") }}
```

<!-- markdownlint-enable MD013 -->

Or use shortcodes in your markdown content:

<!-- markdownlint-disable MD013 -->

```go-template
{{< github-readme-stats/stats class="gh-stats-card" username="schnerring" theme="gruvbox_light" >}}
```

<!-- markdownlint-enable MD013 -->
