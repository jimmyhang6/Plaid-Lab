# plaid-my-first-app

Welcome to the first Plaid Lab!
In this lab session, you'll learn the basics of coding and then get to apply your knowledge to change a bit of code in an existing app.

Let's get started:



## Prerequisites
- Mac laptop
- Download and Install Code Editor: [Atom](https://atom.io/)
![](https://github.com/jimmyhang6/plaid-my-first-app/blob/master/Atom.png)

## Getting Started
1. Download and save [codelab.zip](https://www.dropbox.com/s/pvc074u9g1ybcxk/codelab2.zip?dl=0) (from Dropbox) to your desktop. 

2. Open the zip file (double click) and you should see a '**codelab**' folder which contains the pre-packaged app we'll be using for this session.
  * The '**codelab**' folder should be on your desktop, if not, move it from your '**Downloads**' folder
  * Chrome (browser) may alert you to the file being dangerous and ask if you want to discard it. Click on '**Keep It**'

3. Open the Terminal using these keys: Command+Space; type “terminal”; press Enter)
 * The Terminal will let you run the app we’re using in this codelab
 * You run commands by typing the instructions below and pressing Enter

4. Run this command in the Terminal: `cd ~/Desktop/codelab`
 * It will tell the Terminal to look in the '**codelabs**' folder you’ve just unzipped on your desktop

5. Go to http://localhost:8001 in your Chrome browser
 * The browser is where your web app will be displayed for you to see
 * You should see a website that says “Plaid Quickstart” at the top

At this point the app is running on your laptop!

Now that you have the app running, we'll start to perform a few tasks to connect with Plaid's API and pull the required financial data.

## Connecting a bank account using Plaid Link
1. In your Chrome browser, click on '**Connect with Plaid**'
2. Click '**Continue**' to accept the privacy policy
3. Select a financial instiution by clicking on a logo
4. Type '**user_good**' in the User ID field
5. Type '**pass_good**' in the Password field
6. Click '**Submit**'

The app has now connected to the sample bank account

7. Click the '**Send request**' button to begin retrieving bank data
