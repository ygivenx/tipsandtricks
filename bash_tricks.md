### Here are some 💻 bash tricks 👻

1. Find all folders in the current folder which are in GBs
  ```bash
  - du -h -d 1 . | grep "^\d\+.\d\?G"
  - du -h -d <depth> . | grep "^\d+.\d\?<M|G>" # customize it as you want
  ```
