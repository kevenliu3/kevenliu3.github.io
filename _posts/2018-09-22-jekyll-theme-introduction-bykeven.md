---
layout: post
title: jeky环境搭建
date: 2018-09-23
tags: 环境搭建
---


```
theme -> jekyll theme -> jekyll -> gem -> ruby(devkit)
jekyll server -> bundler && other(error will warning you)
```


1. install ruby(with devkit):ruby installer官网
> install jekyll: gem install jekyll 这里一定要用系统自带的cmd安装，如果用第三方shell终端，例如power shell，容易出现下面错误：


`this problem is probably due to using incompatible versions of the cygwin dll `     
2. cd 到blog的根目录，jekyll server，可能会遇到下面错误：

````
C:/Ruby25-x64/lib/ruby/2.5.0/rubygems/core_ext/kernel_require.rb:59:in `require': cannot load such file -- bundler (LoadError)
````
这里我们采取策略：cannot load such file xxx 我们就gem install xxx       

3. 最后jckyll server运行起来后，访问http://127.0.0.1:4000/即为你的blog。

4. jckyll server遇到的错误
```
C:/Ruby25-x64/lib/ruby/gems/2.5.0/gems/bundler-1.16.5/lib/bundler/runtime.rb:313:in `check_for_activated_spec!': You have already activated rouge 3.2.1, but your Gemfile requires rouge 2.2.1. Prepending `bundle exec` to your command may solve this. (Gem::LoadError)
        from C:/Ruby25-x64/lib/ruby/gems/2.5.0/gems/bundler-1.16.5/lib/bundler/runtime.rb:31:in `block in setup'
        from C:/Ruby25-x64/lib/ruby/2.5.0/forwardable.rb:229:in `each'
        from C:/Ruby25-x64/lib/ruby/2.5.0/forwardable.rb:229:in `each'
        from C:/Ruby25-x64/lib/ruby/gems/2.5.0/gems/bundler-1.16.5/lib/bundler/runtime.rb:26:in `map'
        from C:/Ruby25-x64/lib/ruby/gems/2.5.0/gems/bundler-1.16.5/lib/bundler/runtime.rb:26:in `setup'
        from C:/Ruby25-x64/lib/ruby/gems/2.5.0/gems/bundler-1.16.5/lib/bundler.rb:107:in `setup'
        from C:/Ruby25-x64/lib/ruby/gems/2.5.0/gems/jekyll-3.8.4/lib/jekyll/plugin_manager.rb:50:in `require_from_bundler'
        from C:/Ruby25-x64/lib/ruby/gems/2.5.0/gems/jekyll-3.8.4/exe/jekyll:11:in `<top (required)>'
        from C:/Ruby25-x64/bin/jekyll:23:in `load'
        from C:/Ruby25-x64/bin/jekyll:23:in `<main>'
```

5. 卸载掉不需要的3.2.1
```
`block in verify_gemfile_dependencies_are_found!': Could not find gem 'rake (~> 10.0) x64-mingw32' in any of the gem sources listed in your Gemfile. (Bundler::GemNotFound)
```

```
gem install rake --version=10.0.2
if you still get the error then put this into your gemfile.

gem 'rake', '0.8.7'
```