# vue-tutor-project-intro

## Enabling Vue Development

MacOS:

`brew install node`

Windows:

[NodeJS Installer](https://nodejs.org/en/download/)

## Cloning the repo locally

```
Click Fork on GitHub to fork it your GitHub account, then click the green code button
Select HTTPS and copy the link, then enter the command
git clone PASTE-LINK-HERE
cd vue-tutor-project-intro/tutor-project
npm i
npm run dev
```

This will clone the project down, install it, and host it on your local server. We then need to open another terminal and follow these commands:

```
cd vue-tutor-project-intro/tutor-project
```

From here we will be able to start commiting our work to git and pushing it up

## Setting up your own environment

Following the [Vite](https://next.vuetifyjs.com/en/getting-started/installation/) installation section

Open up VSCode/PyCharm, navigate to the folder that you want to install the project, then, using the terminal then run the following commands in order:

```
npm init @vitejs/app tutor-project -- --template vue
cd tutor-project
npm i
npm run dev
```

Once the above commands are run the terminal is now hosting our server, and we can copy the Local link to be taken to our local server. We now need to open another terminal and navigate back to our folder:

```
cd vue-tutor-project-intro/tutor-project
vue add vuetify
Vite Preview (Vuetify 3 + Vite)
```

Now go back the original terminal and run the below commands:

```
Close server, ctrl + c
npm run dev
```
