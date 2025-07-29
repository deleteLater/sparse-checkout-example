This repository is a demonstration of how to use Git's sparse checkout feature to push a specific directory to a remote repository.

```bash
git clone -n --depth=1 --filter=tree:0 https://github.com/deleteLater/sparse-checkout-example.git && cd sparse-checkout-example
mkdir project_final && cd project_final
vim final.txt
git sparse-checkout set --cone project_final/*
git checkout
git add .
git commit -m "added project_final"
git push
```
