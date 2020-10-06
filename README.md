# Source for lsd-ucsc.github.io 

For the original documentation on the Academic Template for Hugo, [see this repository](https://github.com/wowchemy/wowchemy-hugo-modules).

## System Requirements
You will need to have an updated version of [Golang](https://golang.org/) installed on your machine in order to run Hugo commands.

## Workflow

The **lsd-ucsc.github.io-source** repository contains the editable source code for the **lsd-ucsc.github.io** website. If you want to make a change to the website, it should only be done in this repository instead of directly to the generated website's repository. 

For detailed documentation on how to make changes and build the website, see the [GitHub Pages section of the deployment documentation](https://wowchemy.com/docs/deployment/#github-pages)

The steps to make changes to the template and build the website are as follows: 

- Clone the source repository: `git clone https://github.com/lsd-ucsc/lsd-ucsc.github.io-source.git`
- Init submodule: `cd lsd-ucsc.github.io-source; git submodule update --init --recursive`
- Check that the `public/` folder exists. This contains the content of the generated website. **Do not make changes here**.
- If you want to see the changes you make to the template source code in real time, run `hugo server -D` and go to (by default) `localhost:1313`.
- After you have made the changes you want to make, run `hugo` to generate the website. The website is generated in the `public/` directory. 
- You must now push both the contents of `public/` to the `lsd-ucsc.github.io` repository and the changes you made to the template to this repository. 
- To push the source repo, add all the changes you have made with `git add` **with the exception of the** `public/` **repository**. To see what individual files have changed, use `git status`. Add those that are need, then commit and push: `git commit -m "Your commit message"`, `git push`.
- To push the generated website, change directory to `public/` and `git add *`. Commit and push via `git commit -m "Your commit message"`, `git push`. 

## Making Changes 

Please see [this documentation](https://wowchemy.com/docs/) if you want a deep dive into how to customize the Academic template using the Hugo static site generator. 

Generally, any basic additions can be made by just editing markdown files such as those in the `content/` directory. 

Advanced customization options are available (e.g. JavaScript, CSS/Sass, overriding templates) and details on them can be found in the documentation listed above. 

### Basic Customization

The `content/` directory is where all markdown changes should be made. Currently, the `content/home/` and `content/seminar` directories are where the bulk of the additions have been made. The contents of each directory is listed below alongside a short description and any technical notes regarding its customization.

#### `content/home/`

- `about.md`: The high-level description of the lab that is displayed at the top of the website in the **About** section. 
- `events.md`: The **Events** section of the website that links to the Seminar page.
    - Events should be linked to a separate page on the website that gives an overview of what it is and a schedule for it. This can be done by including a new folder in the `content/` directory that is the name of your event. For example, the LSD Fall Seminar 2020 is linked in `events.md` as `[LSD Seminar Fall 2020](seminar)`, where `seminar` is the name of the folder in `content/` that includes an `index.md` file. The link will go to a page that displays the contents of `index.md`. 
- `faculty.md`: The **Faculty** section which contains pictures of each faculty member of LSD Labs and a link to their personal websites, or a page on the lab's website with more details. 
    - Faculty should have a picture displayed above a link to their personal website. Hugo requires that the image linked follows the format `/img/myfacultyimage.jpg`; however, the location of the image in the repository is `/static/img/myfacultyimage.jpg`.
- `labs.md`: The **Labs** section that lists, and links to, the respective labs of each faculty member. 
- `students.md`: The **Students** section that lists, and links to, the students of LSD Labs. 

#### `seminar/`

- `index.md`: The schedule for the Fall 2020 LSD Seminar. 
