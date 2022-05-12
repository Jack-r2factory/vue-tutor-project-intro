# vue-tutor-project-intro

## Enabling Vue Development

MacOS:

`brew install node`

Windows:

[NodeJS Installer](https://nodejs.org/en/download/)

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

## Cloning the repo locally

```
git clone https://github.com/ASproson/vue-tutor-project-intro.git
cd vue-tutor-project-intro/tutor-project
npm i
npm run dev
```
