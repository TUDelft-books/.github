# Welcome!

This organization contains open interactive textbooks created by employees from Delft University of Technology that are being hosted on GitHub and GitHub Pages. Book websites are shown on: https://oit.tudelft.nl/.

if you'd like to have your book here, request member access to the organisation at one of the owners:
- [Dennis van den Ouden-van der Horst](mailto:d.denouden-vanderhorst@tudelft.nl)
- [Tom van Woudenberg](mailto:t.r.vanwoudenberg@tudelft.nl) 

The owners have a shared responsibility of adding people to the organisation, maintaining the homepage https://oit.tudelft.nl/ and they can be approached for technical questions. This list of owners will grow soon! If you'd like to be an owner, reach out to one of the existing owners!

You can get started on your own account with the Teachbooks Template (https://github.com/TeachBooks/template) and transfer your repository to this organisation as soon as you're a member. After transferring, your book is online at https://oit.tudelft.nl/<book_repository>! As soon as you're a member, you can add new books yourself.

For transferring books you already have somewhere elso on GitHub we propose:
- If the old repository is not shared with others yet:
  - [Transfer repository] to the TUDelft-Books organization.
  - Reactivate GitHub pages from actions by setting the source for GitHub pages to GitHub Actions under `Settings` - `Pages` - `Build and deployment` - `Source` - `GitHub Actions`
  - Run the deploy-book-orkflow from `Actions` - `All workflows` - `call-deploy-book` - `Run workflow` - `Run workflow`
  - Set the repository website as your GitHub Pages website under `Code`- `About` - `Settings icon` - `Website` - `Use your GitHub Pages Website`
- If the old repository is already shared:
  - Use the [GitHub Importer](https://docs.github.com/en/migrations/importing-source-code/using-github-importer/importing-a-repository-with-github-importer) to add it to TUDelft-Books
  - Adding a note: 'Moved to `<link to new repository in TUDelft-books organization>`' to `README.md`
  - Adding a note: 'Moved to `<link to new repository in TUDelft-books organization>`' to the description of the repository on GitHub
  - Adding a banner to the book:
```ymal
sphinx:
  config:
    ...
    html_theme_options:
      ...
      announcement : "This book has been moved to: <a href='https://oit.tudelft.nl/<new repository in TUDelft-book organization>' style='color:white'>https://oit.tudelft.nl/CT1000/2024</a>."
      ...
```
  - Archiving the old repository
  - Reactivate GitHub pages from actions by setting the source for GitHub pages to GitHub Actions under `Settings` - `Pages` - `Build and deployment` - `Source` - `GitHub Actions`:
  - Run the deploy-book-orkflow from `Actions` - `All workflows` - `call-deploy-book` - `Run workflow` - `Run workflow`
  - Set the repository website as your GitHub Pages website under `Code`- `About` - `Settings icon` - `Website` - `Use your GitHub Pages Website`
