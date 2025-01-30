## Boo 👻
Did I jump scare you? Yeah I bet I did. You coward

Holy poop [goboscript](https://github.com/aspizu/goboscript) is so good

---

(for myself):
## Step-by-step reminder of how to make a new goboscript package
1. create a new folder
2. add a 'test' project in it - `goboscript new --name test`
3. MAKE SURE EVERYTHING IS LF, NOT CRLF
4. make the folder for the package (same name as outer folder - package/package)
5. create a gs file in the same directory with the same name (i.e /package/package.gs)
6. Make sure it's LF. If it isn't, then check your vscode settings, and make the default EOL character `\n`
7. Add a readme:
~~~md
  # package.gs
  This is a package library which is built for [goboscript](https://github.com/aspizu/goboscript).
  It is designed to be used with [backpack](https://github.com/aspizu/backpack)
  
  ## Installation
  To use this, make sure to install [backpack](https://github.com/aspizu/backpack)
  
  You can use the package library by adding these lines to goboscript.toml:
  ```toml
  [dependencies]
  package = "https://github.com/FAReTek1/package@<the version you want to use>"
  ```
  
  Then, add this %include to your gs file:
  you can also use this to just %include everything
  ```rs
  %include backpack/package/package
  ```
~~~
8. Use find+replace of 'package' with your package name
9. Add a `goboscript.toml` file containing `[dependencies]`
10. Write your code
11. Use `%include`s in your outer gs file. MAKE SURE TO SEPERATE THEM WITH NEWLINES
12. Make sure everything is using LF
13. Push to a github repository
14. Add a repo description maybe
15. Make a github (pre-)release:
    Description:
    ```
    v0.0.0
    Unbuilt test release.
    ```
16. edit the `test/goboscript.toml` file to add the repo on github.
17. Check for bugs.
