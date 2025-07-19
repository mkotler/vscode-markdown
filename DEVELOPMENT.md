# Instructions to help with development

## How to Build and Deploy the Extension

1. npm install
   -  if it asks for a login it is probably because of a .npmrc that is overriding a registry, then do this:
   -  npm config set registry https://registry.npmjs.org/
   -  then run npm install again
2. npm run build
3. npx nsce package
4. Install the extension in vs code:
   - Press ctrl+shift+p and select Extensions: Install from VSIX
   - Select the .vsix file

## How to manage branches

- All features are created in separate feature branches (e.g., feature/create-checkbox)
- To develop a feature, switch to that branch, make the changes, and commit it in that branch
  - git checkout -b feature/create-checkbox
  - <Make changes>
  - git add .
  - git commit -m "Describe the change"
- Then push the feature branch to remote:
  - git push origin feature/create-checkbox
- Then to test all of the changes together in a staging branch, switch to the branch and merge all feature branches into staging
  - git checkout -b staging
  - git merge feature/create-checkbox
  - git merge feature/change-2
