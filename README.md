I know this is incorrect. But for the life of me i cannot determine how. I have been stuck for months on this situation and i just need to get it out of my head to continue learning. 




TL;DR
Terminal commands to put together a new React Vite project:
npm create vite@latest my-react-app -- --template react
cd my-react-app
npm install
Go into the src/ folder and delete the contents (or leave main.jsx if you understand how to write it yourself already).

Create a main.jsx file and add the minimum entry-point code:

import React from 'react';
import ReactDOM from 'react-dom/client';
import App from './App'; // assuming we use one

ReactDOM.createRoot(document.getElementById('root')).render(
    <React.StrictMode>
        <App />
    </React.StrictMode>
);
Create a App.jsx file and add the minimum component code:
const App = () => {
    return (
        <div>
            <h1>Yoooooooo, is this thing on?</h1>
        </div>
    );
};

export default App;
Back in the terminal:
npm run dev
Open your beautiful app in your browser of choice using the host and port provided to you by Vite in the terminal!
Setting Up Vite
The Source of Truth:
https://vitejs.dev/

To get started with Vite, you need to have Node.js and npm installed on your system. Instead of using create-react-app, we will use Vite to create a new React project.

Command to Create a Vite Project
npm create vite@latest
Then follow the prompts!
Project Name? Whatever you want it to be! I still strongly recommend using lower kebab case (my-project-name).
Select a Framework? React, obviously.
Select a Variant? JavaScript.
Changing Directory and Installing Dependencies
cd <your-app-name>
npm install
Note The <> are placeholders, don't actually write them.
cd <your-app-name> changes your working directory to the newly created project folder.
npm install installs all the necessary dependencies for your project.
Starting the Development Server
To start the development server, run:

npm run dev
This command will start Vite's development server, which is extremely fast due to its optimized build process.
The server will launch your web application and can be accessed at http://localhost:XXXX. The XXXX is whatever port it gives you! Look at your terminal output to see yours.
Shorthand Set Up
npm create vite@latest my-react-app -- --template react
npm create: This command is used to create a new project using a specified template.
vite@latest: Specifies that we want to use the latest version of Vite.
my-react-app: This is the name of your new project. You can change "my-react-app" to whatever name you prefer for your project.
-- --template react: Indicates that we want to use the React template for this project. This sets up the project with all the necessary files and configurations for a React application.
Basic Project Structure
Note: This structure isn’t set in stone and may change over time. Focus on understanding the general layout and purpose of these files and folders, rather than memorizing the exact structure.

After creating a Vite project, the basic project structure will look something like this:

app-name/
+-- node_modules/
+-- public/
+-- src/
¦   +-- assets/
¦   +-- App.css
¦   +-- App.jsx
¦   +-- index.css
¦   +-- main.jsx
+-- .gitignore
+-- .eslintrc.cjs
+-- index.html
+-- package.json
+-- package-lock.json
+-- README.md
+-- vite.config.js
app-name/: This is the root folder of your project. It's named after whatever name you gave your project.
node_modules/: A folder where all the project's dependencies (packages your project needs to run) are stored. You usually don't need to worry about this folder.
public/: A folder for static assets like images and fonts that don’t need to be processed by Vite. These files are available publicly.
src/: This is where your source code lives.
assets/: A folder inside src for images, fonts, or other assets that your components might use.
App.css: This file contains styles specific to the App component.
App.jsx: The main React component of your application, usually where your app starts.
index.css: General styles for your project.
main.jsx: The entry point for your application. This is where your app is first loaded and rendered.
.gitignore: A file that tells Git which files or folders to ignore, so they don’t get tracked in version control.
.eslintrc.cjs: Configuration file for ESLint, a tool that helps you write consistent and error-free JavaScript code.
index.html: The main HTML file for your project. Vite uses this as a template to serve your app.
This is a Single Page Application (SPA), meaning the app loads a single HTML page and dynamically updates it as the user interacts with the app, rather than loading new pages from the server.
package.json: A file that holds various metadata relevant to the project. It includes details like project name, version, and dependencies.
package-lock.json: Automatically generated file that ensures the exact same versions of dependencies are installed every time. It locks the versions of packages.
README.md: A markdown file where you can describe your project, how to set it up, and how to use it. It's a good place to put documentation.
vite.config.js: The configuration file for Vite, where you can customize how Vite behaves and handles your project.
Entry Point
The entry point of a Vite project is main.jsx:

import React from 'react';
import ReactDOM from 'react-dom/client';
import App from './App.jsx';

ReactDOM.createRoot(document.getElementById('root')).render(
    <React.StrictMode>
        <App />
    </React.StrictMode>
);
This file imports React and ReactDOM, as well as the main App component and a CSS file.
ReactDOM.createRoot is used to render the App component into the root DOM element.