# BigDataJunction.github.io
## Setup:

1. Download and install git 
2. git setup 
    ```bash
    git config --global user.name "your name"
    ```
    ```bash
    git config --global user.email youremail@gmail.com
    ```

3. Clone the repo
    ```bash
    git clone https://github.com/BigDataJunction/BigDataJunction.github.io.git
    ```

4. go to the folder 
    ```shell
    cd BigDataJunction.github.io
    ```
5. install  hugo 

    mac:
    ```bash 
    brew install hugo
    
    hugo version

    ```
    windows:
    ```bash 
    choco install hugo
    ```

6. theme setup:
    ```bash 
    git rm -r --cached themes/ananke
    ```
    <!-- ```rm -rf themes/ananke``` -->
    delete contents of .gitmodules 
    ```bash
    git submodule update
    ```

    Install Anakle theme into project  
    ```bash 
    git submodule add https://github.com/theNewDynamic/gohugo-theme-ananke.git themes/ananke
    ```

7. Start Hugo Server / build drafts and run with -D
    ```bash 
    hugo server -D
    ```

8. Create a hugo page/blog
    ```bash 
    hugo new posts/my-first-post.md
    ```

    ```bash 
    Content "\\content\\posts\\my-first-post.md" created
    ```
--------------------------------------------------------------------------
## To cerate a blog 
```bash 
hugo new posts/post_name.md
```

Edit the blog-uri.md file from location 
```nash 
content\\posts\\blog-uri.md
```

Don't forget to make draft == false in .md file.
```md
draft: false
# means blog is ready to be published
```

--------------------------------------------------------------------------


## workflow

1. git checkout dev

```kumarom@KUMARs-Air-2 BigDataJunction.github.io % git checkout dev
M       README.md
Already on 'dev'
Your branch is ahead of 'origin/dev' by 1 commit.
  (use "git push" to publish your local commits)```

2.  Create blog

Create your First Chapter Page
Chapters are meant to be top level pages that contain other child pages. They have a special layout style and often just contain the title and a brief abstract of the section.

Now create your first chapter page with the following command:


```
hugo new --kind chapter basics/_index.md
```

When opening the newly created file content/basics/_index.md, you should see the weight frontmatter with a number. This will be used to generate the subtitle of the chapter page, and should be set to a consecutive value starting at 1 for each chapter level.

Create your First Content Pages
Then create content pages inside the previously created chapter. Here are three ways to create content in the chapter:

```
hugo new basics/first-content/_index.md
hugo new basics/second-content/index.md
hugo new basics/third-content.md
```

Feel free to edit those files by adding some sample content and replacing the title value in the beginning of the files.


```https://mcshelby.github.io/hugo-theme-relearn/basics/branding/index.html```

3. Run the local server and test the blog.

    ```bash 
    hugo server -D
    ```

4. git add and commit

```git status ```

4.1 git add file_name

4.2 git commit -m "msg"


5. Push to dev branch in remote(origin) repo.

```git push origin dev```

6. Only for omkar

Merge dev branch to local main branch

```git checkout main```

```git merge dev```

Run the local server and test the blog.

    ```bash 
    hugo server -D
    ```

7. Push to remote main branch

```git push origin main```


## Final deployment 

url
```https://gohugo.io/hosting-and-deployment/hosting-on-github/```


if not auto deployed:
```md
Github repo--> Action --> Deploy BigDataJunction.. --> Run WorkFlow
```