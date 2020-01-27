## Welcome to Collab CSS

**Purpose:** Base css for all apsc collab sites. It is referenced by all apsc collab sites in production

Apsc collab css is hosted on [github pages](https://apsc-web.github.io/collab-css/). This allows us to remotely reference the repo's css files from github. 

## Apsc Collab Directory Structure
```markdown
apsc_collab_css/
|
|-- modules/                    # for code that is reused often; this includes variables, mixins etc
|   |-- colors.scss
|   |-- fonts.scss
|   ...
|
|-- partials/                   # for code that doesn't need to be compiled to css; e.g buttons, grids
|   |-- _base.scss              # import all variables, mixins etc from modules;
|   |-- _buttons.scss           
|   |-- _nav.scss
|   |-- _headings.scss
|   |-- _sidebar.scss
|   |-- _layout.scss
|   ...
|
|-- vendors/                    #external css or sass from other projects or vendors
|   ...
|
|-- main.css                    #main css file; import all partials using @use rule
```
**Note**: Import variables, mixins etc on _base.css. Do not import these modules on main.css

## Workflow
To make changes to apcs collab base css code (i.e any piece of code on this repository)
1. Clone the repository to your local environment using HTTPS or SSH
```markdown
   git clone https://github.com/apsc-web/collab-css.git 
   ```
2. Checkout a feature branch on the local repository.
  ```git checkout -b <new-branch>```
3. Commit your changes and push to staging/feature branch on github.
```markdown
git commit -m "message"
```
4. Create a pull request to merge staging/master
5. Merge the changes to master


## Additional Notes
While git version control is meant to alievate the pain of accidentaly loosing important code by allowing us to revert dangerous changes, please refrain from editing code on this repository unless your goal is to change the base css code of all collab sites in production.
If your change is site specific, please consider making those changes through custom css

## FAQ's
Why is apsc collab css hosted on github pages? 
This allows us to reference the css directly from github. Doing this allows us to reap the numerous benefits of version control.

## Support
Having trouble? Send an email to web-apsc@ubc.ca and someone will help you sort it out.
