# .NET Blazor WebAssembly project to Github Pages

## Commands to create

- `dotnet new blazorwasm -o BlazorDeploy --pwa` - Create the project
- `dotnet watch run` - Roda o projeto com Hot Reload

## Creating the gitignore

- `dotnet new gitignore`

## Configuring the Repository

- `git init` - start the project as a git repository
- `git add .` - add all created files
- `git branch -M main` - change the name of the master branch to *main*
- `git commit -m "init"` - created the first commit
- `git remote add origin <URL>` - add a github remote repository into the local repository
- `git push -u origin main` - push the local project to the github repository

## Configuring Github Pages into the Github Repository

- Go to `Settings` into the Repository
- Go to `Pages` in the left side
- Go to `Build and deployment` and select the Source `Github Actions`

## Configuring the new route into the code

- Go to `wwwroot` into the project and open `index.html`
- Change the `<base href="/" />` into the index.html to the link of your Github Page
    - `<base href="https://f4nt0.github.io/Blazor_Base_Github_Pages/" />`

## Configuring the Github Actions
- Create a new folder called `.github`
- Create a new folder inside `.github` called `workflows`
- Create a file inside the `workflows` directory called `main.yml`

## Configurin Release
- We need to publish in a folder called `docs`
- `dotnet publish BlazorDeploy.csproj -c Release -o docs --no-logo` is the command to generate the config