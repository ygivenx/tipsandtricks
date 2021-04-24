The data in your mac is spread around into downloads, desktops etc etc... There is python tool `organize-tool` which can help your declutter and organize all your data with simple yaml configuration. 

Thanks to [tfeldmann](https://github.com/tfeldmann) for this awesome tool

Installation: pip3 install -U organize-tool
Github: https://github.com/tfeldmann/organize
Docs: [ReadTheDocs](https://organize.readthedocs.io/en/latest/)

Usage:
`organize config` # opens a file to be edited - I have attached mine below

`organize sim` # simulate the run

`organize run` # run the tool

```yaml
rules:
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
          - tar.gz
      actions:
        - move: ~/Documents/{extension.upper}/
    - folders: ~/Desktop
      filters:
        - filename:
            startswith: "Screen Shot"
      actions:
        - move: ~/Desktop/Screenshots/
    - folders:
          - ~/Downloads
          - ~/Desktop
      filters:
          - filesize: 0
      actions:
          - trash
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

