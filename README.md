# Plaid Lab

Welcome to the first Plaid Lab!
In this lab session, you'll learn the basics of coding and then get to apply your knowledge to change a bit of code in an existing app.

## Terminology
- Code: The information interpreted to create computer software, apps and websites. In order to tell the computer what you want, you have to speak to the computer in a language it understands.
- Language: What the code is written in; There's various languages like Python and Java Script. We'll be using Java Script for this lab.
- Editor: This is what the code is written in. There's lots of text editors from Notepad to Sublime. We'll be using Atom for tihs lab.
- Terminal: An application on your Mac laptop that you input commands into for it to execute upon.
- Browser: This is where the code will be displayed within as part of the web app we're using.

## Tools (Prerequisites)
- Mac laptop
- Download and install a code editor: [Atom](https://atom.io/) (Make sure you add Atom to your 'Applications' folder upon installation)
![](https://github.com/jimmyhang6/plaid-my-first-app/blob/master/Atom.png)

## Getting Started
1. Download the [PlaidLab.zip](https://www.dropbox.com/s/pvc074u9g1ybcxk/codelab2.zip?dl=0) (from Dropbox) to your '**Downloads**' folder. 

2. Open the zip file (double click) and you should see a '**PlaidLab**' folder which contains the pre-packaged app we'll be using for this session.
  * Chrome (browser) may alert you to the file being dangerous and ask if you want to discard it. Click on '**Keep**'
  
  ![](https://github.com/jimmyhang6/plaid-my-first-app/blob/master/PlaidLab%20Zip.png)

3. Open the Terminal using these keys: **Command+Space** then type “**terminal**” and press **Enter**
 * The Terminal will let you run the app we’re using in this Plaid Lab
 * You run commands by typing the instructions below and pressing **Enter**

4. Run this command in the Terminal: `cd ~/Downloads/PlaidLab`
 * This command tells the Terminal to look in the '**PlaidLab**' folder that you’ve just unzipped 

5. Run this command in the Terminal: `/Applications/Atom.app/Contents/Resources/app/atom.sh views/balance.ejs`
 * This command tells Atom to open the **balance.ejs** file that you’ll be editing.
 * If a screen prompt appears asking about Xcode, click on '**Not now**' 
 
 ![](https://github.com/jimmyhang6/plaid-my-first-app/blob/master/XCode.png)
 
6. Run this command in the Terminal: `./run_me.sh` 
 * This command starts the app we’re going to be using on your computer 
 * If asked if you want to accept network connections, click '**Allow**'
 
7. Now click on this UR **http://localhost:8001** which will open your Chrome browser
 * The browser is where the web app will be displayed for you to see
 * You should see a webpage that says '**Welcome to the Plaid Lab App!**' at the top

:thumbsup: At this point the app is running on your laptop! :thumbsup:

Now we'll start to perform a few tasks to connect with Plaid's API and pull the required financial data.

## Connecting a bank account using Plaid Link
To access essential financial data, you'll need to connect a sample bank account to the web app using Plaid Link.

1. In your Chrome browser, click on '**Connect with Plaid**'
2. Click '**Continue**' to accept the privacy policy
3. Select a financial institution by clicking on any logo on the screen :bank:
4. Type '**user_good**' in the user ID field
5. Type '**pass_good**' in the password field
6. Click '**Submit**' (The app has now connected to the sample bank account)
7. Click the '**Send request**' button to begin retrieving bank data
 * In this case, we're making a request using the **/balance endpoint** to retrieve current balances

## Editing the code - Part 1
Now in the web browser, you'll seeing the account balances for the sample account we connected using Plaid. If you take a closer look, you may notice a typo. We're now going to edit the code to correct the typo on the page.

1. Go back to the Atom window and make sure '**index.ejs**' is selected at the top of the window
 * This is one of the two files that control the app you’re seeing
 
![](https://github.com/jimmyhang6/plaid-my-first-app/blob/master/Screen%20Shot%202018-10-11%20at%202.47.12%20PM.png)
 
2. Now that you see the code, can you find where the typo is?
<details>
 <summary>Need help?</summary>
It says “Ttoal balance” instead of “Total balance”.
</details>
3. Once you spot the typo, correct it by typing in the correct spelling
4. Type '**Command+S**' to save your changes to the code
5. Go back to your Chrome browser and type '**Command+R**' to refresh the browser
 * Note: You will be prompted to re-conenct the sample account using Plaid Link (user_good/pass_good)
6. Check to see that your code change has been applied in the browser

Congratulations! You’ve fixed your first bug!

![](https://github.com/jimmyhang6/plaid-my-first-app/blob/master/Total%20Balance%20Typo%20Fixed.png)

## Editing the code - Part 2

1. In the Chrome browser where you see your web app, you’ll notice that the total balance is reported as 1,000,000,000 instead of the actual total balance.

![](https://github.com/jimmyhang6/plaid-my-first-app/blob/master/Total%20Balance%20Number.png)

2. Now go back to Atom and look at Lines 13-46 (these numbers may change) from index.ejs which contains the code that shows the accounts and balances
3. Before we can fix them, let’s take a quick break to go over some programming fundamentals:  
 * HTML is a language that controls website layout
 * The quickstart app we are using uses HTML tables
 * HTML tables are made up of rows (tr) and cells (td)
 * The word strong tells the browser which words to  emphasize
 * Follow this [link](https://codepen.io/tiberiusf/pen/rqwzYj) to see an example of HTML tables in action. Feel free to take some time to change or add rows. Keep in mind the sum won’t auto-update - not to worry! 

 ![](https://github.com/jimmyhang6/plaid-my-first-app/blob/master/HTML%20Tables.png)
 
 * We also need functions: code formulas that take inputs and transform them into outputs
 * Follow this link to see examples of a function that squares a number
