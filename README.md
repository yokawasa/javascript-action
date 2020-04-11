# Quickstart JavaScript Action

```
# Install the dependencies
npm install

# run the test
npm test

# Change action.yml (contains defines the inputs and output for your action)
# reference: https://help.github.com/en/actions/automating-your-workflow-with-github-actions/metadata-syntax-for-github-actions
vi action.yml

# Change the code
vi index.ts
```

Actions are run from GitHub repos. Now you can package the action and release for distribution
```
npm run package

# Since the packaged index.js is run from the dist folder, you need to add dist
git add dist

# Create release branch
git checkout -b v1
git commit -a -m "v1 release"
git push origin v1
```

Now you can consume the action with yml file like this:

```yaml
uses: actions/javascript-action@v1
with:
  milliseconds: 1000
```
