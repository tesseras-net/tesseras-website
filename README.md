# Tesseras Website

Source for the [Tesseras](https://tesseras.net) website, built with
[Zola](https://www.getzola.org/).

## About

The public website for the Tesseras project — a P2P network for preserving human
memories across millennia. The site includes project information, news posts,
FAQs, release notes, and mailing list subscriptions. Content is available in
English and Brazilian Portuguese.

## Usage

### Prerequisites

- [Zola](https://www.getzola.org/) — static site generator
- [just](https://just.systems/) — task runner
- [dprint](https://dprint.dev/) — formatter for Markdown and TOML

### Development

```sh
# Serve locally with live reload
just serve

# Build the site
just build
```

### Deployment

```sh
just deploy
```

## Links

- [Website](https://tesseras.net)
- [Documentation](https://tesseras.net/book/en/)
- [Source code](https://git.sr.ht/~ijanc/tesseras-website) (primary)
- [GitHub mirror](https://github.com/tesseras-net/tesseras-website)
- [Ticket tracker](https://todo.sr.ht/~ijanc/tesseras)
- [Mailing lists](https://tesseras.net/subscriptions/)

## License

ISC — see [LICENSE](LICENSE).
