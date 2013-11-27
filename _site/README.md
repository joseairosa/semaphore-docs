# Semaphore documentation

[Semaphore](https://semaphoreapp.com) is a hosted continuous integration and deployment service. This repository contains the source of its [help and documentation site](http://docs.semaphoreapp.com).

This is a Rack app powered by [Jekyll](http://jekyllrb.com) and hosted on Heroku.

### Installation

Install all dependencies:

    bundle install --path .bundle

Run the Jekyll server:

    bundle exec jekyll --server 4000 --auto

Point your browser to [http://localhost:4000](http://localhost:4000) and view the site.

### Writing

Markdown is preferred. When embedding images, create a directory `assets/images/page-name` for the page that you are writing.

### Contributing

1. Fork the repo.
2. Type away new words. See the Installation and Writing sections above.
3. Commit both the changes to the source file and the generated `_site/`. That is how we are able to publish content on Heroku.
3. Push to your fork and submit a pull request.

Please [file an issue](https://github.com/renderedtext/semaphore-docs/issues) if you:

- have a suggestion on how the documentation could be improved,
- would like to point out that something is not clear, or
- find something painfully missing.

Thanks!

-- [Rendered Text](http://renderedtext.com)
