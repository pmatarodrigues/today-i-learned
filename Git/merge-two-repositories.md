# Merge Repository A into Repository B

```bash
cd path/to/PROJECT-B
git remote add project-a path/to/PROJECT-A
git fetch PROJECT-A --tags
git merge --allow-unrelated-histories PROJECT-A/master # or whichever branch you want to merge
git remote remove PROJECT-A
```
