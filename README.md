# Plaid Lab

Welcome to the first Plaid Lab!
In this lab session, you'll learn the basics of coding and then apply your knowledge to change a bit of code in an existing app.

## Terminology
- Code: The information interpreted to create computer software, apps and websites. In order to tell the computer what you want, you have to speak to the computer in a language it understands.
- Language: The conventions for how code is written. There's various languages like Python and Javascript. We'll be using Javascript for this lab.
- Editor: This is the software that you use to write the code in. There's lots of text editors from Notepad to Sublime. We'll be using Atom for this lab.
- Terminal: An application on your Mac laptop that lets you input commands and then executes those commands.
- Browser: This is where your web app will be displayed for you to interact with it.

## Required Tools
- Mac laptop
- Download and install a code editor: [Atom](https://atom.io/) (Make sure you add Atom to your 'Applications' folder upon installation)
![](https://github.com/jimmyhang6/plaid-my-first-app/blob/master/Atom.png)

## Getting Started
1. Save and download the [PlaidLab.zip](https://www.dropbox.com/s/jzii4f2z0wdlh1j/PlaidLab.zip?dl=0) file (from Dropbox) to your '**Downloads**' folder. 

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
 * If a screen prompt appears asking about Xcode, click on '**Not Now**' 
 * Feel free to close other windows like the Atom welcome screen - you'll focus on the **balance.ejs** file
 
 ![](https://github.com/jimmyhang6/plaid-my-first-app/blob/master/XCode.png)
 
6. Run this command in the Terminal: `./run_me.sh` 
 * This command starts the app we’re going to be using on your computer 
 * If asked if you want to accept network connections, click '**Allow**':
 
  ![](https://github.com/jimmyhang6/Plaid-Lab/blob/master/accept_network_connections.png)
 
7. Now open this URL in a new tab in your Chrome browser: **http://localhost:8001** 
 * The browser is where the web app will be displayed for you to see
 * You should see a webpage that says '**Welcome to the Plaid Lab App!**' at the top

:thumbsup: At this point the app is running on your laptop! :thumbsup:

Now we'll start to perform a few tasks to connect with Plaid's API and pull the required financial data.

## Connecting a bank account using Plaid Link
To access financial data, you'll need to connect a sample bank account to the web app using Plaid Link.

1. In the new tab in Chrome that you created (http://localhost:8001), click on '**Connect with Plaid**'
2. Click '**Continue**' to accept the privacy policy
3. Select a financial institution by clicking on any logo on the screen :bank:
4. Type '**user_good**' in the user ID field
5. Type '**pass_good**' in the password field
6. Click '**Submit**' 
7. Click '**Continue**' (The app has now connected to the sample bank account)
8. Click the '**Go**' button to begin retrieving bank data
 * In this case, we're making a request using the **/accounts/get endpoint** to retrieve the account and balance information

## Change the app by editing the code - Part 1
Now in the web browser, you'll see all the balances for the sample account we connected using Plaid. If you take a closer look, you'll notice a typo on the page. We're now going to edit the code to correct the typo.

<details>
 <summary> Need help finding the typo? </summary>
It says “Ttoal balance” instead of “Total balance”.
</details>
<br/>

1. Go back to the Atom window 
2. Now that you see the code, can you find which part in the code the typo is located at?
<details>
 <summary> Need help finding the typo? </summary>
You can use Command+F to search in Atom for the typo or refer to line 37
</details>
<br/>

3. Once you spot the typo, type in the correct spelling
4. Type '**Command+S**' to save your changes to the code
5. Go back to your Chrome browser and type '**Command+R**' to refresh the browser
 * Note: You will be prompted to re-connect the sample account using Plaid Link (user_good/pass_good)
6. Check to see that your code change has been applied in the browser

Congratulations! You’ve fixed your first bug! 

![](https://github.com/jimmyhang6/plaid-my-first-app/blob/master/Total%20Balance%20Typo%20Fixed.png)

## Change the app by editing the code - Part 2

1. In the Chrome browser where you see your web app, you’ll notice that the total balance is reported as 1,000,000,000 instead of the actual total balance.

![](https://github.com/jimmyhang6/plaid-my-first-app/blob/master/Total%20Balance%20Number.png)

2. Now go back to Atom and look at **lines 18-62** which contains the code that shows the accounts and balances
3. Before we can fix them, let’s pause to go over some programming fundamentals:  
 * HTML is a language that controls website layout
 * The quickstart app we are using uses HTML tables
 * HTML tables are made up of rows (tr) and cells (td)
 * The word strong tells the browser which words to  emphasize
 * See below or follow this [link](https://codepen.io/tiberiusf/pen/rqwzYj) for an example of HTML tables in action. Feel free to change or add rows. Keep in mind the sum won’t auto-update - not to worry! 
 ```
 <!-- The table starts here -->
<table>
  <!-- This is a table row. Columns are generated automatically
       as long as each row has the same number of cells.
  -->
  <tr>
    <!-- This is a table cell -->
    <td><strong>Name</strong></td>
    <!-- This is another cell -->
    <td><strong>Balance</strong></td>
  </tr>
  <!-- The first row ends here, and more follow below. -->
  <tr>
    <td>Checking Account</td>
    <td>$100</td>
  </tr>
  <tr>
    <td>Savings Account</td>
    <td>$200</td>
  </tr>
  <tr>
    <td><strong>Total balance:</strong></td>
    <td>$300</td>
  </tr>
<!-- The next line means we're done with the table -->
</table>
```
 
 * We also need functions: code formulas that take inputs and transform them into outputs
 * See below or follow this [link](https://codepen.io/tiberiusf/pen/yRXzGj) for an example of a function that adds numbers together
```
// A function is like a formula that transforms its inputs into an output.
// This function has three inputs, and the output is their sum.
function sum(firstNumber, secondNumber, thirdNumber) {
  // This line just means that it adds the three numbers and reports their sum.
  return firstNumber + secondNumber + thirdNumber;
};

function run() {
  // This sets the input to 3, 2, 7, which makes it print 12 (3 + 2 + 7) below.
  // Can you change some of the inputs to other numbers and see what happens?
  return sum(3, 2, 7);
}; 
```
 * Now let’s put the HTML table and function together which is how the app shows the account names, balances and total sum.
 * See below or follow this [link](https://codepen.io/tiberiusf/pen/vVZWKy) for an example of how functions can be used to create tables. 
 ```
 // Time to reinforce your knowledge about functions and tables!
//
// This function creates another table, like the previous snippet
// (https://codepen.io/tiberiusf/pen/rqwzYj), but instead of
// creating the table directly it creates it by combining the
// outputs of other, smaller functions.
function createTable() {
  return '<table>' +
            // getHeader (see below) creates table headers
            createHeader() +
            // getRow (see below) creates table rows with
            // the account names and balances you give it.
            createRow('Checking account', 100) +
            createRow('Savings account', 200) +
         '</table>';
}

// createHeader (used above in createTable) returns the header.
function createHeader() {
  return `<tr>
            <td><strong>Name</strong></td>
            <td><strong>Balance</strong></td>
         </tr>`;
}

// createRow (used above in getTable) has two inputs (the name
// and the balance) and uses them to create a row.
function createRow(accountName, balance) {
  return '<tr>' +
            '<td>' + accountName + '</td>' +
            '<td>' + balance + '</td>' +
          '</tr>';
}

// This function is the glue that puts everything together.
// You can just ignore it; it's not relevant to the codelab.
function run() {
  return createTable();
}
 ```
Now that you understand HTML tables and functions, let’s switch back to Atom to fix the incorrect toal balance.

4. In Atom, find **line 59** it passes totalBalance as the input to a function. However,the total balance is set to 1,000,000,000 on **line 47** which is incorrect.
5. Replace **1,000,000,000** with **0** on **line 47** for now - we’ll then have to calculate the right total balance

 * Before we can do that, we need just a little more programming background
 * See below or follow this [link](https://codepen.io/tiberiusf/pen/dgRezm?editors=0010) for an example of using a loop to computer the sum of account balances

```
// In the function below we will use a for loop (represented
// by the word "forEach") to compute the sum of some account balances.
// Ignore the "run" function itself - it's required boilerplate.
function run() {
  // Initially the total balance is 0, because we haven't added anything yet.
  let totalBalance = 0;
  // This is the list of balances we want to add up. In real apps, these
  // will come from the API. For example: let balances = data.accounts.accounts;
  let balances = [100, 200, 300];
  
  // The next line goes through the balances: "for each" balance,
  // do something with it. (add it to the total balance)
  balances.forEach(
    // accountBalance represents the balance currently being processed.
    accountBalance => {
      // This line adds the current number to the running total balance.
      totalBalance += accountBalance;
    }
  );
  
  // Here we're done and report the total balance we've calculated.
  // You can try changing some of the numbers from the list above
  // (or even adding or removing some numbers) to see the sum change.
  return totalBalance;
};
```
6. Now back in Atom, try to see if you can update the loop to get the right total balance
<br/>
<details>
 <summary> Need help? </summary>
Each account’s balance is available inside the for loop (lines 50-57). Can you now calculate the total balance?
</details>
<br/>

<details>
 <summary> Need more help? </summary>
To get the right toal balance, you need to add accountBalance to totalBalance inside the loop
</details>
<br/>

<details>
 <summary> What's the right total balance? </summary>
If you see $44,910, awesome! That’s the right answer!
</details>
<br/>
