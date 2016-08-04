# Deploying a New Release

*This will take place anytime the dev team sends a new version for deployment.*

## Prep
- Create release branch (vX.XX) off of develop version in github repo
- Test with `gulp build` locally

## Deploy
- Open the site in SharePoint Designer
- Grab the `dist` folder from a the release you want to deploy
- Copy `dist` folder into the `app/version` folder
- Rename the `dist` folder to the version number

## Test
- Test out the release using these [guidelines](testing.md).  
- If tests pass please proceed to the next step, if not please notify lead developer

## Set as Default
- Copy/paste `index.html` into the same folder & rename to `default.aspx`
        (*this keeps the index.html at the version folder so if necessary you can test out older versions at a later time.*)
- move `default.aspx` to root of site.  Confirm yes if asked to overwrite the existing default.aspx (*This sets the default app at the root to the newest version.*)
