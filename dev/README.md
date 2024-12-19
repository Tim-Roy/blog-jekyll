# Notes about creating the site

- forked minimal-mistakes theme

`bundle exec jekyll serve --livereload` doesn't work - keep getting the following error and can't figure out a resolution. So just running `jekyll serve`

> /home/tim/.local/share/gem/ruby/3.0.0/gems/jekyll-4.3.3/lib/jekyll.rb:29:in `require': cannot load such file -- json (LoadError)

### Kill running on port

If I accidently close the terminal and the server is still running, I can manually kill it by:

1. Get pid of service running on port 4000

```
lsof -i:4000
```

2. Kill pid

```
kill -9 <pid>
```

bundle exec jekyll serve --livereload