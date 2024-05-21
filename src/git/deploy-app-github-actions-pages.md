# Deploy app using github pages

## Step1: Modify package.json

Add below line with app corresponding name
"homepage": "https://diasraphael.github.io/google-clone"

In scripts
"predeploy": "npm run build",
"deploy": "gh-pages -d build"

## Step2: Install packages

npm install gh-pages

## Step3: In github go to the repo settings

select pages and choose master under branch and save

## Step4: deploy

npm run deploy
