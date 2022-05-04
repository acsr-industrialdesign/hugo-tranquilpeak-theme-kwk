---
title: "Hugo Installation"
date: 2022-05-02T18:57:15+02:00
draft: true
thumbnailImagePosition: left
thumbnailImage: /images/powersystem.jpg

---

## The world’s fastest framework for building websites

Hugo is one of the most popular open-source static site generators. With its amazing speed and flexibility, Hugo makes building websites fun again.
<!--more-->

{{< toc >}}

{{< wide-image src="/images/powersystem.jpg" title="[PowerSystem]" >}}

### [Installation](https://gohugo.io/getting-started/installing/)

	- Installed on [[MBP15acsr]] via homebrew at /usr/local/Cellar/hugo/0.97.3
		- [[20220420]] [[Installation]][[Hugo]] on [[MBP15acsr]] via [[Homebrew]]
	-
	  > Replace `brew install hugo` with `brew install hugo --HEAD` if you want the absolute latest in-development version.

	- brew should have updated your path to include Hugo. You can confirm by opening a new terminal window and running a few commands:

	  ```
	  		  $ # show the location of the hugo executable
	  		  which hugo
	  		  /usr/local/bin/hugo
	  		      
	  		  # show the installed version
	  		  ls -l $( which hugo )
	  		  # at MBP15acsr:
	  		  lrwxr-xr-x  1 astro  admin  30 Apr 20 12:33 /usr/local/bin/hugo -> ../Cellar/hugo/0.97.3/bin/hugo
	  		  
	  		  # verify that hugo runs correctly
	  		  hugo version
	  		  # Hugo Static Site Generator v0.13 BuildDate: 2015-03-09T21:34:47-05:00 # from example
	  		  hugo v0.97.3+extended darwin/amd64 BuildDate=unknown  # at MBP15acsr
	  ```

#### Next Steps [](https://gohugo.io/getting-started/installing/#next-steps)

	  Now that you’ve installed Hugo, read the [Quick Start guide](https://gohugo.io/getting-started/quick-start/) and explore the rest of the documentation. If you have questions, ask the Hugo community directly by visiting the [Hugo Discussion Forum](https://discourse.gohugo.io/).

{{< wide-image src="/images/biogas.jpg" title="[Biogasanlage]" >}}

### [Setup](https://gohugo.io/getting-started/quick-start/)

### Quick Start

Create a Hugo site using the beautiful Ananke theme.

- This quick start uses [[macOS]] in the examples. For instructions about how to install Hugo on other operating systems, see [install](https://gohugo.io/getting-started/installing).
- It is required to have [Git installed](https://git-scm.com/downloads) to run this tutorial.
- For other approaches to learning Hugo (like books or video tutorials), refer to the [external learning resources](https://gohugo.io/getting-started/external-learning-resources/) page.

#### Step 1: Install Hugo

- DONE Check installed version

### Step 2: Create a New Site 

```
mkdir -p /Users/astro/github/Hugo
cd /Users/astro/github/Hugo
hugo new site quickstart
```

The above will create a new Hugo site in a folder named ``quickstart``.
- output:

  ```
    Congratulations! Your new Hugo site is created in /Users/astro/github/Hugo/quickstart.

    Just a few more steps and you're ready to go:

    1. Download a theme into the same-named folder.
        Choose a theme from https://themes.gohugo.io/ or
        create your own with the "hugo new theme <THEMENAME>" command.
    2. Perhaps you want to add some content. You can add single files
        with "hugo new <SECTIONNAME>/<FILENAME>.<FORMAT>".
    3. Start the built-in live server via "hugo server".

    Visit https://gohugo.io/ for quickstart guide and full documentation.
  ```

### Step 3: Add a Theme 
	  
See themes.gohugo.io for a list of themes to consider. This quickstart uses the beautiful Ananke theme.

- First, download the theme from GitHub and add it to your site’s themes directory:

    ```
    cd quickstart
    git init
    git submodule add https://github.com/theNewDynamic/gohugo-theme-ananke.git themes/ananke
    ```

- Then, add the theme to the site configuration:

    ```
    echo theme = \"ananke\" >> config.toml
    ```

- output:
    
    ```
    Cloning into '/Users/astro/github/Hugo/quickstart/themes/ananke'...
    remote: Enumerating objects: 2496, done.
    remote: Counting objects: 100% (519/519), done.
    remote: Compressing objects: 100% (286/286), done.
    remote: Total 2496 (delta 261), reused 403 (delta 199), pack-reused 1977
    Receiving objects: 100% (2496/2496), 4.45 MiB | 4.83 MiB/s, done.
    Resolving deltas: 100% (1358/1358), done.
    ```

### Step 4: Add Some Content 
	  
You can manually create content files (for example as `content/<CATEGORY>/<FILE>.<FORMAT>`) and provide metadata in them, however you can use the `new` command to do a few things for you (like add title and date):

-  ```
    hugo new posts/my-first-post.md
    ```

- output:

    ```
    Content "/Users/astro/github/Hugo/quickstart/content/posts/my-first-post.md" created
    ```

- Edit the newly created content file if you want, it will start with something like this:
		  
    ```
    ---
    title: "My First Post"
    date: 2019-03-26T08:47:11+01:00
    draft: true
    ---
    ```

    > Drafts do not get deployed; once you finish a post, update the header of the post to say `draft: false`. More info [here](https://gohugo.io/getting-started/usage/#draft-future-and-expired-content).


### Step 5: Start the Hugo server [](https://gohugo.io/getting-started/quick-start/#step-5-start-the-hugo-server)

Now, start the Hugo server with [drafts](https://gohugo.io/getting-started/usage/#draft-future-and-expired-content) enabled:

    ```
    ▶ hugo server -D

                    | EN
    +------------------+----+
    Pages            | 10
    Paginator pages  |  0
    Non-page files   |  0
    Static files     |  3
    Processed images |  0
    Aliases          |  1
    Sitemaps         |  1
    Cleaned          |  0

    Total in11 ms
    Watching for changes in /Users/bep/quickstart/{content,data,layouts,static,themes}
    Watching for config changes in /Users/bep/quickstart/config.toml
    Environment: "development"
    Serving pages from memory
    Running in Fast Render Mode. For full rebuilds on change: hugo server --disableFastRender
    Web Server is available at http://localhost:1313/ (bind address 127.0.0.1)
    Press Ctrl+C to stop
    ```

Navigate to your new site at [http://localhost:1313/](http://localhost:1313/).

Feel free to edit or add new content and simply refresh in browser to see changes quickly. (You might need to force refresh your web browser, something like Ctrl-R usually works.)

## Hugo Theming

- {{query((property type [[Hugo Theme]]))}}

### [[Hugo]] 300+ Themes

[[20220420]] preselected [[Hugo Theme]] for [[180.323 KWK Webauftritt]] #.ol-nested

- [[Tranquilpeak]]

    - Hugo version of Tranquilpeak is a based on original Hexo version https://github.com/LouisBarranqueiro/hexo-theme-tranquilpeak. This version is simply a port to Hugo static site generator.
    - #### For people who want to create their own version of tranquilpeak (developers) [](https://themes.gohugo.io/themes/hugo-tranquilpeak-theme/#for-people-who-want-to-create-their-own-version-of-tranquilpeak-developers) #.ol
        - Run 
            > `git clone https://github.com/kakawait/hugo-tranquilpeak-theme.git`

        - Follow [developer documentation](https://github.com/kakawait/hugo-tranquilpeak-theme/blob/master/docs/developer.md) to edit and build the theme

- Postponed

    - Blist
    - Tella
    - Split

- Original [Split](https://onepagelove.com/split) Template by [One Page Love](https://onepagelove.com/)
