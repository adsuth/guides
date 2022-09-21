# JS 0 - Setting Up

## Node.js vs Javascript

Node JS is the command-line equivalent of Javascript. Vanilla Javascript is purely for browsers; it can only be run on HTML pages. Node.js doesn't have that limitation, and can be used for a variety of purposes, including creating Command Line Interface programs (CLI). That's what we'll be starting with first, just to learn the basic syntax.

## Environment

I'm just going to list the most likely environments you'll use:

| Name    | **Link**                                      | Reason                                                                                                     | Alternatives                                                                                                                         |
|:-------:|:---------------------------------------------:| ---------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------ |
| VSCode  | [VSCode Link](https://code.visualstudio.com/) | Lightweight, lots of good extensions, integrated Git support...                                            | Atom (discontinued due to Microsoft aquisition of )                                                                                  |
| Repl.it | [Repl.it](replit.com/~)                       | Browser-based IDE for a variety of languages. Simple, out of the box CLI programming. Good for quick tests | Look up "JS browser IDE" and you'll likely find an alternative.<br/>Perhaps the only downside of Repl is that it requires an account |

## Github

You're going to want a Github account. Not initially, but when you start tackling larger projects, its version control capabilities are invaluable.

Set one up at [Github](https://github.com/)

**TBC**

## Installing Node.js

*Just a quick note: I refer to the "terminal" through this part. This will be different depending on your Operating System. For Windows: Command Prompt. For Mac and Linux: Terminal*

*VSCode has an integrated terminal - accessed by going to Terminal > New Terminal, or by using the shortcut: `Ctrl+'`.*

*Occasionally, VSCode commands may not return anything (eg: `node --version`. In those cases, just use your PC's terminal.*

If you do not have Node installed on your machine, you'll need to do so in order to run any node programs you write.

To check, run the following command in your PC's terminal:

`node --version`

If it responds with a version number, eg: `v17.4.0`, you already have node installed. 

Otherwise, it will not recognise node as a command. In that case, you'll want to install it by downloading it from Node's own site [Node.js](https://nodejs.org/en/). 

(get the LTS version. That stands for "Long-Term Support")

### Suggestions for Working in VSCode CLI

I suggest you create a new folder for your practice. Before we start learning HTML and CSS, you can create a simple environment that'll **refresh every time you save your file** by using a package called `nodemon`.

First, you need to initialise your folder with npm.

Open the terminal and run:

`npm init -y`

Once that finishes, install nodemon with the following command:

`npm i nodemon`

When that's done, go to the generated `package.json` file, and replace this line

```json
"test": "echo \"Error: no test specified\" && exit 1"
```

with this

```json
"start": "nodemon -e js,json index.js"
```

- `-e js,json` tells nodemon to restart the app when you save a file with the following extensions. In this case, `.js` and `.json`.

- `index.js` is the name of the file nodemon will run.

Finally, run this command to start the app:

`npm start`
