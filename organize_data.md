## 🔖 Organize your computer 🖥 now!


The data 💿 in your mac 💻 is spread around into downloads, desktop etc etc... There is a **python** 🐍 tool `organize-tool` which can help your declutter and organize all your data with a simple yaml configuration. 

Thanks 😄 to [tfeldmann](https://github.com/tfeldmann) for this awesome 😎 tool

Installation: `pip3 install -U organize-tool`

💫 Github: https://github.com/tfeldmann/organize

📚 Docs: [ReadTheDocs](https://organize.readthedocs.io/en/latest/)

🚗 Usage 👋🏼: 

`organize config` # opens a file to be edited - I have attached mine below

`organize sim` # simulate the run

`organize run` # run the tool

```yaml
rules:
    # move files to folder according to extension
    - folders:
        - ~/Downloads/**/*
        - ~/Desktop/**/*
      filters:
        - extension:
          - pdf
          - docx
          - jpg
          - pptx
          - xlsx
          - mov
          - mp4
          - m4a
          - png
          - heic
          - csv
          - jpeg
          - json
          - key
          - zip
      actions:
        - move: ~/Documents/{extension.upper}/
    # Move screenshots to a dir
    - folders: ~/Desktop
      filters:
        - filename:
            startswith: "Screen Shot"
      actions:
        - move: ~/Desktop/Screenshots/
    # remove empty files
    - folders:
          - ~/Downloads
          - ~/Desktop
      filters:
          - filesize: 0
      actions:
          - trash
    # remove partial downloads
    - folders: ~/Downloads
      filters:
          - extension:
                - download
                - crdownload
                - part
                - dmg
          - lastmodified:
                days: 2
                mode: older
      actions:
          - trash
    # remove duplicate files
    - folders:
        - ~/Desktop
        - ~/Downloads
        - ~/Documents
      subfolders: true
      filters:
        - duplicate
      actions:
        - echo: "{path} is a duplicate of {duplicate}"
        - trash
    - folders:
      - ~/Programming
      subfolders: true
      filters:
        - extension:
          - python
      actions:
        - echo: "{path.base}"
```

