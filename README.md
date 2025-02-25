## Steps

- Moves duplicated steps of deploy workflow to a composite action (see [action/cache-deps](.github\actions\cached-deps\action.yml))
- Creates a javacript based action (see [action/deploy-s3-javascript](.github\actions\deploy-s3-javascript\action.yml))
  - Inside deploy-s3-javascript it was run `npm init -y` and installed specific github actions `npm install @actions/core @actions/github @actions/exec`
  - NOTE: node_modules inside custom js actions shouldn´t be in git ignore file, because github actions won't install the dependencies before execution. It is expected that all required dependencies are available
  - When building custom actions, its needed to checkout code before run action

 