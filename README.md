## Welcome to Collab CSS

**Purpose:** Base css for all apsc collab sites. It is referenced by all apsc collab sites in production
**collab css Github Pages: [https://apsc-web.github.io/collab-css/](https://apsc-web.github.io/collab-css/)

Apsc collab cs is hosted on github pages. This allows us to reference the repository directly from github. 

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
|   |-- _base.scss              # import all variables, mixins etc from modules; do not import these into main css files
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

## Workflow
To make changes to apcs collab base css code (i.e any piece of code on this repository)
1. Clone the repository to your local environment using SSH or HTTPS
2. Checkout a staging branch on the local repository. If adding completely new css code (e.g a new layout), please create a new feature branch instead. Once you have made changes on the staging/feature branch, please commit your changes and push to staging/feature branch on github.
3. Create a pull request to merge staging/master
4. Merge the changes to master
5. If all is well, you can safely delete the feature branch


## Additional Notes
While github exists for version control which is meant to alievate the pain of having to revert dangerous changes, please refrain from editing code on this repository unless your goal is to change the base css code of all collab sites in production.
If your change is site specific, please consider making those changes through custom css

## FAQ's
Why is apsc collab css hosted on github pages? 
This allows us to reference the css directly from github. Doing this allows us to reap the numerous benefits of version control.


## Support
Having trouble? Send an email to web-apsc@ubc.ca and someone will help you sort it out.
