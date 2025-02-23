# Welcome!

This organization contains open interactive textbooks created by employees from Delft University of Technology that are being hosted on GitHub and GitHub Pages. Book websites are shown on: https://oit.tudelft.nl/. Furthermore, this homepage lists TU Delft open interactive textbooks hosted on various other place, among others:
- other GitHub personal/organizations with corresponding GitHub pages
- EWI pages (prime.pages.ewi.tudelft.nl)
- published TU Delft OPEN Interactive textbooks (interactivetextbooks.tudelft.nl)
- ...

if you'd like to have your book here, request member access to the organisation at one of the owners:
- [Dennis van den Ouden-van der Horst](mailto:d.denouden-vanderhorst@tudelft.nl)
- [Tom van Woudenberg](mailto:t.r.vanwoudenberg@tudelft.nl) 

The owners have a shared responsibility of adding people to the organisation, maintaining the homepage https://oit.tudelft.nl/ and they can be approached for technical questions. This list of owners will grow soon! If you'd like to be an owner, reach out to one of the existing owners!

You can get started on your own account with the template provided by TeachBooks, converted to be used at TU Delft (https://github.com/TUDelft-books/TUDelft-template) and transfer your repository to this organisation as soon as you're a member. After transferring, your book is online at https://oit.tudelft.nl/<book_repository>! As soon as you're a member, you can add new books yourself.

For transferring books you already have somewhere elso on GitHub we propose:
- If the old repository is not shared with others yet:
  - [Transfer repository](https://docs.github.com/en/repositories/creating-and-managing-repositories/transferring-a-repository) to the TUDelft-Books organization.
- If the old repository is already shared:
  - Use the [GitHub Importer](https://docs.github.com/en/migrations/importing-source-code/using-github-importer/importing-a-repository-with-github-importer) to add it to TUDelft-Books. If your repository is not public, you have to add credentials or create an empty repo and push your local repository to this new one.
  - In the old repoistory:
    - Adding a note: 'Moved to `<link to new repository in TUDelft-books organization>`' to `README.md`
    - Adding a note: 'Moved to `<link to new repository in TUDelft-books organization>`' to the description of the repository on GitHub
    - Adding a banner to the book with a link to your new online book, see code below
    - Archive the old repository
  - In the new repository in the TUDelft-books organization:
    - reactivate GitHub pages from actions by setting the source for GitHub pages to GitHub Actions under `Settings` - `Pages` - `Build and deployment` - `Source` - `GitHub Actions`
    - If your new repository is private: create a new Personal Access Token (classic) with at least the scopes `repo`, `read:org` and `gist` as described in the [github documentation](https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/managing-your-personal-access-tokens), and add this token with the name `GH_PAT` as a `Repository secret` or `Organization secret` (`Settings` - `Secrets and variables` > `Actions` > `Repository secrets` or `Organization secrets`.)
    - Copy [repository variables for deploy-book workflow](https://github.com/TeachBooks/deploy-book-workflow?tab=readme-ov-file#customize-the-workflow-teachbook-releasing-settings) from old repository
    - Run the deploy-book-orkflow from `Actions` - `All workflows` - `call-deploy-book` - `Run workflow` - `Run workflow`
    - Set the repository website as your GitHub Pages website under `Code`- `About` - `Settings icon` - `Website` - `Use your GitHub Pages Website`
    - Copy other GitHub-specific repository settings from the old repository.
    - Adapt the `baseurl` and `repository_url` in `_config.yml`:
      - `baseurl        : "https://oit.tudelft.nl/<new repository name>"`
      - `repository_url : "https://github.com/TUDelft-books/<new repository name>"` 
```ymal
sphinx:
  config:
    ...
    html_theme_options:
      ...
      announcement : "This book has been moved to: <a href='https://oit.tudelft.nl/<new repository in TUDelft-book organization>' style='color:white'>https://oit.tudelft.nl/<new repository in TUDelft-book organization> </a>."
      ...
```
