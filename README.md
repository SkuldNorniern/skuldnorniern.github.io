# Skuld Norniern's Council!
A place for programmers who have interest in Skuld Norniern's Project!

## 1. Generating github.io page 

  1. Create Username.github.io 
  2. Clone it to the local repository
  3. Add index.html file for test
  4. do the git push for test perpose

## 2. Jekyll Installation
  
  1. Install Ruby 
  2. Install Jekyll, bundler by using Gem
    I recommand Jekyll 3.8 ※ Github pages don't support 4 or higher yet
  ```bash
  gem install jekyll bundler
  ```
  3. Check the version of the Jekyll 
  ```bash
  jekyll -v
  ```
  4. Setup new Jekyll project 
  ```bash
  jekyll new . --force
  ```
  5. Run Jekyll Project
  ```bash
  bundle exec jekyll serve
  ```
  ### Jekyll Webrick Error
  
  > 'require': cannot load such file -- webrick (LoadError)

  ```bash
  bundle add webrick
  ```

  ### Jekyll rexml Error
  
  > 'require': cannot load such file -- rexml/parsers/baseparser
  ```bash
  bundle add rexml
  ```

## 3. Applying theme

        jekyll-theme-yat : https://github.com/jeffreytse/jekyll-theme-yat
        
        Unsupported by github pages
        
        Simple Green Techblog : https://github.com/alainpham/alainpham.github.io

        The one that i pick.

        copy all the files (except of _pages) and paste it on your repo and push it


 ## 4. Adding Comments
 
 ### In case of using the Simple Green Techblog
    In _data/settings.yml
    you can find 
    ```
        disqus:
            comments: true
            disqus_shortname:
    ```
    just put your disqus account shorname next to the disqus_shortname:

    also if you want to disable the comments on the main page
    create a new layout called post 
    copy the default to post but on the default remove the
    ```html
    {% include disqus.html %}
    ```