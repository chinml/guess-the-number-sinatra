# Guess The Number web edition
Different versions of the Guess The Number game for TechLadies pre-bootcamp workshop #2

Guess the Number is a basic ruby application built on top of Sinatra for the purposes of TechLadies pre-bootcamp workshop #2, which covers the basics of the web, HTML and CSS. We will also cover some basic Git concepts and how to deploy the app onto Heroku. Given that everyone may be using different machines with different operating systems, we will be using Cloud9 as our development environment.

## Resources used
- [GitHub](https://github.com)
- [Nitrous](https://www.nitrous.io/)
- [Heroku](https://www.heroku.com)

## Getting set up

### On GitHub
1. Sign up for a GitHub account.
2. Go to the [Guess The Number project repository](https://github.com/TechLadies/guess-the-number-sinatra) and fork it by clicking the Fork button in the top right corner (ask for help if you can't find it).
3. Leave this window open as you will need to perform further set up actions to integrate smoothly with Nitrous or Cloud9.

### Setting up SSH between Github and Cloud9
3. Sign up for a Cloud9 account by clicking on the GitHub icon in the top right corner. You will need to authorize Cloud9 to use your Github account.
4. Once it's done, you will be at the Dashboard page.
5. Go to `https://c9.io/account/ssh` to access your SSH Settings page.
7. Open another window and go to `https://github.com/settings/keys` to access your SSH and GPG keys on Github.
8. Click on the green New SSH key button in the top right corner.
9. Enter "Cloud9 IDE" in the Title field.
10. Switch back to the SSH Settings page in the previous window and copy everything in the grey box. Paste the contents in the Key field on your SSH and GPG keys page on Github.
11. Click on the green Add SSH key button.

### On Cloud9
4. Click on Create New Workspace.
5. Enter a name for your workspace and a brief description.
5. Fill in `git@github.com:<YOUR_USER_NAME>/guess-the-number-sinatra.git` in the field Clone from Git or Mercurial URL (optional). This is the repository that you forked to your own account in the earlier steps.
6. Select Ruby for the Choose a template option.
7. Click on the green Create Workspace button to proceed.
8. You should see a loading window, and this may take a while, so keep the window open and let it run.
9. When things are set up, you should see your workspace, with a file manager in the left column, a text editor taking up most of the space in the main right area and a smaller terminal in the bottom of the right area.
10. To run the app, enter `ruby app.rb -p $PORT -o $IP` in the terminal and press enter.

### On Nitrous
3. Sign up for a Nitrous account by clicking on the Sign Up button in the top right corner. It will take some time for your account to be set up.
4. Once it's done, click on your profile image in top right corner and select Account Settings.
5. Connect your account GitHub, and fill in the Name and Email field under Git Config on the Account Settings page. Remember to click on Save Changes.
6. Click on the Dashboard link in the top left corner to return to the Dashboard, then click on the Plus icon to create a new project.
7. Name your project, and choose the Ruby template, then click the Create Project button. This will take some time to complete.
8. Once it's done, click on Open IDE.

### On integrating with GitHub
4. Click on Git in the toolbar and select Clone from GitHub. Select guess-the-number-sinatra and click Clone.
5. When the terminal prompt asks "Are you sure you want to continue connecting (yes/no)?", type "yes" and press enter.
    ![](https://www.chenhuijing.com/filerepo/tl-ws2-terminal.png)
6. Your files should now appear under nitrous > code > guess-the-number-sinatra in the left sidebar.

### On running the development server
1. Run `bundle install` to install the required ruby dependencies.
    ![](https://www.chenhuijing.com/filerepo/tl-ws2-terminal2.png)
2. Start the server by running `bundle exec ruby ./app.rb`
3. You should see something like this in the terminal
```
[2016-08-11 16:31:24] INFO  WEBrick 1.3.1
[2016-08-11 16:31:24] INFO  ruby 2.3.1 (2016-04-26) [x86_64-linux]
== Sinatra (v1.4.7) has taken the stage on 3000 for development with backup from WEBrick
[2016-08-11 16:31:24] INFO  WEBrick::HTTPServer#start: pid=683 port=3000
```
4. Click on Preview in the toolbar and select `Port 3000 - HTTP`. This should launch a separate window with the app running.

### On Heroku
1. Sign up for a Heroku account by clicking Sign Up in the top right corner.
2. After verifying your email and setting your password, proceed to the dashboard.
3. Click on the New button on the top right, click Create New App button, leave the defaults and click Create App.
    ![](https://www.chenhuijing.com/filerepo/tl-ws2-heroku.png)
4. For Deployment Method, select the Connect to GitHub option.
5. Click the Connect to Github button and authorize Heroku to have access to your GitHub account information.
6. Search for the guess-the-number-sinatra repository and click the Connect button.
7. If you choose to Enable Automatic Deploy, then every time you commit a change to your repository, Heroku will deploy those changes.
8. You can also choose to manually deploy your app.
