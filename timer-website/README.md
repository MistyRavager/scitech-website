## Guide on File Structure
#### Summary  
There are 4 main portions: The main config.toml file, the data (.yml) files, the css files for styling, and the html files. 
-  **config.toml**: It has two main sections:
    - The first section is for the various navbar items, like home, about etc. The urls can either route to a different section in the same page (if prefixed by a #) or different subpages (if prefixed by a /) 
    - The second section is for the various sections in the main page, like about, projects (*portfolio*) etc. The data for all the headings and paragraphs (barring the individual project and team member cards) is also present here.
- **data files**: The data for the various pages is present in different parts of the code:
    - Main page: As mentioned earlier, the data present in the various sections in the main page is mostly present in the config.toml file
    - /data : This contains the data for the various sub-pages. Much of this is irrelevant, and has been commented out. The data for the team-member cards is present in team.yml (it uses images from static/images/team) and the data for the project/portfolio cards is present in gallery.yml (it uses images from static/images/portfolio)
    - Data for the blogs: The data for the various blogs is present in the .md files in content/blog
    - Data for the projects: The data for the various projects is present in the .md files in content/portfolio
- **css files**: All of the css is present in assets/css/style.css . This file has been copied from themes/timer-hugo and only this file should be modified. Bootstrap items can be modified using `!important`
- **html files**: The various html files are present in the 'layouts' directory. The html files in layouts/partials are used for elements/sections that appear across many pages, like the about-section, contact-section etc.
The html file for the main page is index.html. The subpages use a combination of the html files from the `_default` directory, and the files from the relevant sub-directory (egs: timer/site/portfolio uses the portfolio sub-directory). 
