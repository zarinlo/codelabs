# Codelabs Repository

## Overview

This is where I host any google-like codelab I create, which can be found on my website: [zarin.io](https://zarin.io/)

To understand more about the local environment required to set this up, please read: [Publish Technical Tutorials in Google Codelab Format](https://medium.com/@zarinlo/publish-technical-tutorials-in-google-codelab-format-b07ef76972cd)

## Logistics

- Codelabs are written in markdown (i.e. `.md` files)
- Exported to google-codelab style using `claat export name_of_markdown_file.md`
- In the `index.html` file under the folder created as a result of the `claat export` command, before hosting on github pages, make sure you modify the `<script>` and `link` tags like so: 
    ```html
    # before 
    <script src="../../bower_components/webcomponentsjs/webcomponents-lite.js"></script>
    <link rel="import" href="../../elements/codelab.html">

    # after
    <script src="../bower_components/webcomponentsjs/webcomponents-lite.js"></script>
    <link rel="import" href="../elements/codelab.html">
    ```
- Run python simple server using `python -m SimpleHTTPServer` in the root directory, then navigate to the folder resulting from the `claat export` command to see the codelab on your browser on: http://localhost:8000/
