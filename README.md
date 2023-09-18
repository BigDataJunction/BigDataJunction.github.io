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
hugo new posts/blog-uri.md
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
## Final deployment 
if not auto deployed:
```md
Github repo--> Action --> Deploy BigDataJunction.. --> Run WorkFlow
```
