# BigDataJunction.github.io
Setup 

1. Download and install git 
2. git setup 
```git config --global user.name "your name"```
```git config --global user.email youremail@gmail.com```

3. Clone the repo
```git clone https://github.com/BigDataJunction/BigDataJunction.github.io.git```

4. go to the folder 
```cd BigDataJunction.github.io```
5. install  hugo 
    mac:
    ```brew install hugo```
    windows:
    ```choco install hugo```

theme setup:
```git rm -r --cached themes/ananke```
<!-- ```rm -rf themes/ananke``` -->
delete contents of .gitmodules 
```git submodule update```

6. Install Anakle theme into project  
```git submodule add https://github.com/theNewDynamic/gohugo-theme-ananke.git themes/ananke```
-----------------------------setup done---------------------------------------
6. Start Hugo Server / build drafts and run with -D
```hugo server -D```

7. Create a hugo page 
```hugo new posts/my-first-post.md```

```Content "bigdatajunction\\content\\posts\\my-first-post.md" created```
-----------------------------------------------------------------------------
To cerate a blog 
```hugo new posts/blog-uri.md```

edit the blog-uri.md file from location 
```content\\posts\\blog-uri.md```

dont forget to make draft == false in .md file.
```draft: false```

