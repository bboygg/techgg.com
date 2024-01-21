# 💻 techgg.com 
A Blog about my tech journey


## How to create Posts
To create a new post, run the following command:
```
hugo new posts/my-first-post.md
```

## How to Run Local Server 
#### 1. Initialize the Main Project
Since I'm using the theme in the submodule, I need to initialize the main project and submodules.
Run the following command at project directory.
```
git submodule init 
git submoudle update
```

#### 2. Initialize the Theme Submodule
Run the following command at submodule dicrectory (where theme is located.)
```
git submodule init
git submodule update
```

#### 3. Start Hugo Server
Run the following command at main project directory.
```
hugo server -D
// The -D flag includes content marked as draft, which can be useful during development.
```

It will be like 
```
 ~/bboygg/techgg.com hugo server -D  
Watching for changes in /Users/user/bboygg/techgg.com/{archetypes,assets,content,themes}
Watching for config changes in /Users/user/bboygg/techgg.com/config.toml
Start building sites … 
hugo v0.121.2-6d5b44305eaa9d0a157946492a6f319da38de154+extended darwin/arm64 BuildDate=2024-01-05T12:21:15Z VendorInfo=brew


                   | EN-GB  
-------------------+--------
  Pages            |    16  
  Paginator pages  |     0  
  Non-page files   |     0  
  Static files     |     5  
  Processed images |     1  
  Aliases          |     1  
  Sitemaps         |     1  
  Cleaned          |     0  

Built in 37 ms
Environment: "development"
Serving pages from memory
Running in Fast Render Mode. For full rebuilds on change: hugo server --disableFastRender
Web Server is available at http://localhost:1313/techgg.com/ (bind address 127.0.0.1) 
Press Ctrl+C to stop
```