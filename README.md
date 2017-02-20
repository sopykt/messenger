# Creating your own Facebook Messenger bot


Facebook recently opened up their Messenger platform to enable bots to converse with users through Facebook Apps and on Facebook Pages. 

You can read the  [documentation](https://developers.facebook.com/docs/messenger-platform/quickstart) the Messenger team prepared but it's not very clear for beginners and intermediate hackers. 

So instead here is how to create your own messenger bot in 15 minutes.

## Get set

Messenger bots uses a web server to process messages it receives or to figure out what messages to send. You also need to have the bot be authenticated to speak with the web server and the bot approved by Facebook to speak with the public.

You can also skip the whole thing by git cloning this repository, running npm install, and run a server somewhere.

### *Build the server*

1. Create new folder and cd to that directory.
2. Install the Heroku toolbelt from here https://toolbelt.heroku.com to launch, stop and monitor instances. Sign up for free at https://www.heroku.com if you don't have an account yet.
    ```
    sudo apt-get install software-properties-common # debian only

    sudo add-apt-repository "deb https://cli-assets.heroku.com/branches/stable/apt ./"

    curl -L https://cli-assets.heroku.com/apt/release.key | sudo apt-key add -

    sudo apt-get update

    sudo apt-get install heroku

    ```  
2. Install Node from here https://nodejs.org, this will be the server environment. Then open up Terminal or Command Line Prompt and make sure you've got the very most recent version of npm by installing it again:

    ```
    sudo npm install npm -g
    ```

3. Let's create a new Node project. Hit Enter to accept the defaults.

    ```
    npm init
    ```

4. Install the additional Node dependencies. Express is for the server, request is for sending out messages and body-parser is to process messages.

    ```
    npm install express request body-parser --save
    ```

5. Now clone my codes from github

    ```
    git clone https://github.com/sopykt/messenger.git
    ```
6. Add my heroku repo 
    
    ```
    git remote add heroku https://git.heroku.com/serene-badlands-46223.git
    ```
7. Now you are ready and start editing. When finished push back your edited code to heroku repo by doing this. You might not need `git init` if you already done it once.
    ```
    git init

    git add .

    git commit -m 'that what edited'

    git push heroku master

    ```