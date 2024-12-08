# Wikijs PDF Exporter

Welcome to the wikijs exporter, these scripts enable you to export any file from the wiki (given that your account has the right permissions to see them). And with no API required, just your browser's JWT token :000

To use correctly this project follow the instructions one by one.

## How to use in Github Codespaces (easier to set up, overall a lot slower)

- Open this repository in [Github Codespaces](https://github.com/codespaces)
- Update the config.yml file with your wikijs site informations. 
    - ~~or, you can run the wikijs container provided in this repository by running `task up`.~~ this may not work as codespaces require github authentication when accessing the site.
- Update the `.env` file with your [WikiJS JWT token](#how-to-get-the-jwt-token)
- run `sudo chmod 777 ./out` to allow write access to the `./out` directory.
- run `task pdf:export` to export the site pages to PDF in the `./out` directory.

## How to run on local machine (a whole lot faster, but requires a couple extensions on VScode)

**Prerequisites**: Docker & DevContainer Extensions in VSCode

1. Open this repository in VSCode
2. Open the Command Palette (Ctrl+Shift+P or Cmd+Shift+P on Mac)
3. Select "Dev Containers: Reopen in Container"
4. Run the `task pdf:export` task

## How to get the JWT token

1. Open your browser's Developer Tools (F12 or right-click > Inspect > Applications Tab > Cookies > http://localhost:3000)
2. Login to your wikijs
3. Copy the value of the `jwt` cookie
4. Paste it in the `.env` file
