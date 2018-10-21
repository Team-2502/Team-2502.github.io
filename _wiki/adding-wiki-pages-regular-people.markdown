---
layout: post
title:  "How to add wiki pages (for non-programmers)"
category: Meta
---

1. Make a GitHub account. If you are on the programming team, you should already have one. You can make a GitHub account [here](https://github.com/).

1. Ask the programming lead to add you to the Team-2502 Github organization

1. Once you are added to the Team-2502 organization, you will be able to manipulate the repositories for the team. 
    This will allow you to add issues to our issue tracker, but more relevantly, it will allow you to add new wiki pages. 
    To do so, you will have to navigate to the [repository for the wiki](https://github.com/Team-2502/Team-2502.github.io).
    <br  />
    
    When you get to the repository's home page, it should look something like this:
    
    ![Image of front page of wiki repository]({{ "assets/wiki-repo-homepage.png" | absolute_url}})

1. Think about what kind of wiki page you will make. 
    1. If it's a wiki page related to build, navigate to the `_build` directory. 
    1. If it's related to maintaining this wiki, navigate to the `_wiki` folder. 
    1. If it's related to programming, navigate to the `_programming` directory.
    1. If it's related to scouting/strategy, navigate to the `_strategy` directory.
    <br  />
    
    * To navigate to a directory, click on its name.  
    * Normally, there shouldn't really be a reason that you need to use any of the other folders.
    * By putting your wiki page in the correct folder, you ensure that people are easily able to find your wiki page.
    
    This wiki page belongs in the `_wiki` folder because it is about how to add pages to this wiki, so I clicked on the `_wiki` page.
  
1. Make a new file in the directory by clicking the "Create new file button". 

    ![Image of the Create New File button]({{ "assets/create-new-file-create-wiki-page.png" | absolute_url}})

1. Give your new file a file name. Ensure the name is all lowercase, has no spaces (use hyphens instead), and briefly describes the purpose of the page. 
For example, the file name of this wiki page is `adding-wiki-pages-regular-people.markdown` Note that the filename *must* end in `.markdown`.
The file name will not be shown to people looking at the wiki.

    ![Image of the filename textbox]({{ "assets/set-file-name-make-wiki-page.png" | absolute_url}})

1. Now, you need to add some YAML front matter. This tells the wiki a little bit about your page so it can be displayed correctly. YAML front matter goes at the beginning of your file and looks like

    {% highlight yaml %}
    ---
    layout: post
    title:  "How to add wiki pages (for non-programmers)"
    category: Meta
    ---
    {% endhighlight %}

   You can copy-paste the above text into the big textbox like shown.
    
   ![Image of front-matter in big text box]({{ "assets/insert-front-matter-create-wiki-page.png" | absolute_url }})
    
    
1. Set the title to something meaningful. The title is the thing that will be displayed to wiki readers, so keep it descriptive and sensible.

1. Set the category to something reasonable. The wiki groups pages of the same category together.
Do your best to keep your page within the existing categories. 

1. Write the rest of your wiki page as you see fit. The wiki uses Markdown formatting, which will let you add subheadings, bullet points, and so forth. To learn about how to use Markdown, click [here](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet).

1. Commit your new file to the `master` branch.

1. After a short period, your page will be visible on the wiki!


If you want to add images to your wiki page, [follow these instructions](\{\{"_wiki/adding-images-to-wiki-pages.markdown" | absolute_url}}).
We use a program called Jekyll for our wiki. Check out the [Jekyll docs][jekyll-docs] for more info on how to get the most out of Jekyll. File all bugs/feature requests at [Jekyll’s GitHub repo][jekyll-gh]. If you have questions, you can ask them on [Jekyll Talk][jekyll-talk].

[jekyll-docs]: https://jekyllrb.com/docs/home
[jekyll-gh]:   https://github.com/jekyll/jekyll
[jekyll-talk]: https://talk.jekyllrb.com/
