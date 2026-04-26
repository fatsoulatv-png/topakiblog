source "https://rubygems.org"

# This is the github-pages gem — keeps you in sync with what GitHub Pages
# actually builds remotely. You only need to `bundle install` if you want to
# preview the site locally; GitHub Pages builds it for you on push.
gem "github-pages", group: :jekyll_plugins

# Plugins
group :jekyll_plugins do
  gem "jekyll-feed"
  gem "jekyll-sitemap"
  gem "jekyll-seo-tag"
end

# Windows / JRuby compatibility (harmless on macOS/Linux)
platforms :mingw, :x64_mingw, :mswin, :jruby do
  gem "tzinfo", "~> 1.2"
  gem "tzinfo-data"
end
