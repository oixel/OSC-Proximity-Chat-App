# OSC-Proximity-Chat-App
We're making an app that allows you to talk to people within a set radius around you, anonymously. You could use this to easily chat with people at very populated places, like a library or dining hall on campus.

[Drop ideas into the planning doc](https://docs.google.com/document/d/1fnZhzdzapjkcn7T2G9LytV6WGVBb7rkJRJlz3hdv6NY/edit?usp=sharing) (Google Docs)

[Design plans](https://www.figma.com/file/2mvddKeA4XMODdCidYkDid/Proximity-Chat-App) (Figma)

## Developer instructions
### Install Node.js
First, make sure you have the latest stable version of Node.js installed on you system.

Then, fork this repository and run `git clone <url of forked repo>`.

**Linux**

Install [Node Version Manager](https://github.com/nvm-sh/nvm#installing-and-updating) (Github) and follow the installation instructions. Check to see if your distro's package manager carries nvm before this, though.

After `nvm` is installed run `nvm install node` and then `nvm use node`.

**Windows**

Install Linux immediately

### Client
Install the ExpoGo app from the Google Play Store or App Store on your phone.

`cd` into `client` and install the dependencies: `npm install`.

Use `npm start` to start the program and scan the QR code using the ExpoGo App (Android) or the Camera App (iOS).

### Server
Set up a Firestore instance

1. Log into a Google account you wish to use for development
2. Go to https://firebase.google.com/ and click "Get started"
3. Click "add a project"
4. Type in a project name, click continue
5. Disable Google Analytics, click create project
6. When the project is done being created, click the settings icon in the sidebar and then "Project settings"
7. Underneath the "Your apps" section, click the web development icon (looks like `</>`)
9. Type a name in for your app, do not check the Firebase Hosting box and click "register app"
10. Copy the listed configuration keys into `/server/config_example.md`, and rename the file to `.env`
11. Click continue to console, and go to Build > Firestore Database on the sidebar, and click create database
12. Select the nam5 server, and click next
13. Start in test mode, click enable
14. Create two collections, one named `messages` and another named `users`
  * Make a document with random information to create the collections. The fields won't matter as the correct ones will be added via the functions of our app itself
15. While running the server, the database should be connected and good to go! For more information on how our database works, look at [ApiChecklist.md](https://github.com/ufosc/OSC-Proximity-Chat-App/blob/main/ApiChecklist.md) and see the Firestore documentation at https://firebase.google.com/docs/firestore/

Installing dependancies

`cd` into `server` and install the dependencies: `npm install`.

While working, run `npx tsc` to compile the typescript code into the `build` directory as Javascript. Or run `npx tsc -w` in a seperate terminal to recompile on file changes.

Start the server: `npm start`.

## Contributing
Please read [CONTRIBUTING.md](https://github.com/ufosc/OSC-Proximity-Chat-App/blob/main/CONTRIBUTING.md).
