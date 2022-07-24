# DoReMi Subscription - Geektrust
####  DoReMi is a streaming app which allows users to listen to music, podcasts and watch videos. They offer different subscription plans for different categories of services.

### Users can subscribe to any of these plans. 
- A user can choose only one plan per category. 
- All plans, by default, can only be streamed on one device. 

### Music streaming subscription plans 
- FREE	PERSONAL	PREMIUM
 1 month Trial	 Rs.100 for 1 month	 Rs. 250 for 3 months
 Video streaming subscription plans 

- FREE	PERSONAL	PREMIUM
 1 month Trial	 Rs.200 for 1 month	 Rs. 500 for 3 months
 Podcast streaming subscription plans 

- FREE	PERSONAL	PREMIUM
 1 month Trial	 Rs.100 for 1 month	 Rs. 300 for 3 months

### Top Up
- DoReMi allows users to add a top up to increase the number of devices that they can stream to for an additional cost.
- A user can choose only one top up.  
- The subscribed top up is applicable for all subscriptions. 
- A top up can be added only when a subscription exists.
 
FOUR_DEVICE	TEN_DEVICE
Upto 4 Devices	 Upto 10 Devices
Total cost: Rs.50 for 1 month	 Total cost: Rs.100 for 1 month

### Renewal Reminder
Once a user subscribes to a plan, the user needs to be notified 10 days before the plan expires.
  
### Goal
Given a date when the subscription starts, your program should print: 
- The date on which the reminder should be sent for each subscription category 
- The total amount for renewal. Renewal amount is the sum of all the subscription plan amount and top up amount. 

- 💡 Pro tip: Aim to get the Readability and Correctness (I/O) badges - your profile can go forward with most companies with those 2 badges. The rest can be improved upon later!

### Assumptions
- A user can buy only one category of subscription at a time. 
- By default all plans can only be streamed on one device 
- A user can buy only one category of top up at a time. 
- One top up applies to all the subscriptions being bought. 
 
### Input Commands & Format
Your program should take as input the start date for subscriptions, subscriptions plans to be added, top up to be added.

START_SUBSCRIPTION DD-MM-YYYY 
ADD_SUBSCRIPTION SUBSCRIPTION_CATEGORY PLAN_NAME 
ADD_TOPUP TOP_UP_NAME NO_OF_MONTHS 
PRINT_RENEWAL_DETAILS 

#### Examples :
START_SUBSCRIPTION 20-02-2022 
ADD_SUBSCRIPTION MUSIC  PERSONAL 
ADD_SUBSCRIPTION VIDEO PREMIUM 
ADD_TOPUP ADD_TOPUP 
PRINT_RENEWAL_DETAILS

### Output Commands & Format
- Your program should print the renewal date for each subscription category and the total renewal amount on executing the command PRINT_RENEWAL_DETAILS.
 
RENEWAL_REMINDER SUBSCRIPTION_CATEGORY DD-MM-YYYY 
RENEWAL_AMOUNT AMOUNT 
#### Examples :
RENEWAL_REMINDER MUSIC 10-03-2022  
RENEWAL_REMINDER VIDEO 10-05-2022 
RENEWAL_AMOUNT 700
 

### Sample Input/Output 1
- INPUT
START_SUBSCRIPTION20-02-2022
ADD_SUBSCRIPTIONMUSIC PERSONAL
ADD_SUBSCRIPTIONVIDEO PREMIUM
ADD_SUBSCRIPTIONPODCAST FREE
ADD_TOPUPFOUR_DEVICE 3
PRINT_RENEWAL_DETAILS

- OUTPUT
RENEWAL_REMINDERMUSIC 10-03-2022
RENEWAL_REMINDERVIDEO 10-05-2022
RENEWAL_REMINDERPODCAST 10-03-2022
RENEWAL_AMOUNT750
#### Explanation
- Music Streaming for 1 Month [Personal plan]  -       100
- Video Streaming  for 3 Month [Premium plan]  -       500
- Podcast Streaming  for 1 Month Trial [Free plan]  -    0
- FOUR_DEVICE’s for 3 months (50 X 3)  -               150
- Total   -                                            750


### Error Scenarios
- When a user adds the same category of subscription or top up twice or more, error_code should be printed. Error code should be printed when the date format is wrong.
 
### Error Scenarios & Error Codes 



### Pre-requisites
* NodeJS 12.6.0/14.15.4/16.10.0
* npm

### How to run the code
We have provided scripts to execute the code. 
- Use `run.sh` if you are Linux/Unix/macOS Operating systems and `run.bat` if you are on Windows.  Both the files run the commands silently and prints only output from the input file `sample_input/input1.txt`. You are supposed to add the input commands in the file from the appropriate problem statement. 
- Internally both the scripts run the following commands 
 * `npm ci --silent` - This will build the solution downloading the necessary dependencies.
 * Once the `npm install` from the previous build process is complete, we will execute the program using the command
- `npm start --silent sample_input/input1.txt`
- We expect your program to take the location to the text file as parameter. Input needs to be read from a text file, and output should be printed to the console. The text file will contain only commands in the format prescribed by the respective problem.
- This main file, main.go should receive in the command line argument and parse the file passed in. Once the file is parsed and the application processes the commands, it should only print the output.

### Running the code for multiple test cases
- Please fill `input1.txt` and `input2.txt` with the input commands and use those files in `run.bat` or `run.sh`. Replace `./geektrust sample_input/input1.txt` with `./geektrust sample_input/input2.txt` to run the test case from the second file. 

 ### How to execute the unit tests
- Mocha based test cases are executed with the following command from the root folder
`mocha test`
- Jest based test cases are executed with the following command from the root folder
`jest`

### Typescript
- Your main file should be named as `geektrust.ts`.
- As of now we only support Typescript under the NPM build system. This will require you to compile your typescript program into javascript.
- We run the commands `npm install --silent`, `npm start --silent` and `npm test --silent`.
- Please ensure that the npm install commands creates the file `geektrust.js` from your geektrust.ts file. The npm start command should then execute this `geektrust.js` file.
- In your `package.json` file make sure you have an entry for the install, start and test script.
* The install command should install the dependencies and also build the `geektrust.js` file.
* The start command will execute the program.
* The test command should execute all the unit tests present

```
"scripts": {
    "install" :"<command to create your geektrust.js file>",
    "start": "node geektrust.js",
    "test": "mocha"
}
```

Note: If you create the geektrust.js file in some other folder (like dist/, build/ or out/)other than the main folder, then please appropriately edit the start command.

### Help
- You can refer our help documents [here](https://help.geektrust.com)
- You can read build instructions [here](https://github.com/geektrust/coding-problem-artefacts/tree/master/NodeJS)
