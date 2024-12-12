# Hack the Mainframe

EmptyStack Solutions is planning to dump massive amounts of heavy metals into a nearby lake. Use your terminal to hack the mainframe and stop them before it's too late! In this workshop, you'll practice using terminal commands to navigate a file system, read files, and search for data.

## Getting Started

1. Use your file manager or VS Code to create a `block02` folder in your `coursework` directory.
2. Navigate your terminal to the `block02` folder.
3. Download the files and folders you'll need for this workshop by running this command:
   ```
   git clone https://github.com/FullstackAcademy/Unit1.HackTheMainframe.git
   ```
4. `cd Unit1.HackTheMainframe` to navigate into the folder that you just downloaded.
5. Run `pwd` to verify that you are in the correct directory. The output should end with `/block02/Unit1.HackTheMainframe`.

## Find the restaurant

You know that the engineers at EmptyStack Solutions get dinner together at a local restaurant. You have a device that can scan their employee badges, but you don't remember the name of the restaurant. However, you know that it starts with the word "Fork". You also know that "Alice" and "Bob" are engineers at EmptyStack Solutions. Use your terminal to find the name of the restaurant.

1. `cd restaurants` to get into the `restaurants` directory.
2. `ls` will show you a list of restaurants.
3. Use `cd name_of_restaurant` to go into a restaurant.
   1. For example, to visit **The Big Plate**, you would run `cd the_big_plate`.
4. Use `ls` inside a restaurant to see a list of customers.
5. Use `cd ..` to go back out.
6. Explore! What is the name of the restaurant you're looking for?
7. Take a screenshot of your terminal once you've found the restaurant.

> [!TIP]
>
> If you're ever lost, use `pwd` and `ls` to figure out where you are and what's around you.

> [!IMPORTANT]
> You will submit all screenshots at the end of the workshop.

## Scan employee badges

Great! You've found the restaurant. Now, let's try scanning the EmptyStack employee badges. If you're lucky, someone might have forgotten to encrypt their badge. You're trying to get an ID number that you can use to access their EmptyStack Solutions account.

1. Navigate your terminal into the restaurant you found earlier.
2. Try scanning Alice's badge: `cat alice`.\
   If you see `XXXXXXXXXXXXXXXXXXXXXX`, then you're on the right track! You'll have to scan someone else's badge, though. Alice is too smart to leave her badge unencrypted.
3. Once you've scanned an unencrypted badge and found an ID number, take a screenshot of your terminal.
4. Write the ID down. You'll need it in the next section.

> [!TIP]
>
> `cat` is short for "concatenate". The command reads the contents of a file and _concatenates_ them to the terminal output.

> [!TIP]
>
> You can press `Tab` to autocomplete a file or directory name. For example, if you type `cat a` and then press `Tab`, the terminal will autocomplete the command to `cat alice`.

## Find the password

The ID is a good start, but you'll need a password as well to access the account. Luckily for you, EmptyStack Solutions recently had a massive security breach. All of their accounts have been exposed in a plaintext file, which you'll find conveniently in the `emptystack` directory.

1. Navigate your terminal to the `emptystack` directory.
2. Use `ls` to see the contents of the directory.
3. Use `cat` to read the contents of the `accounts.txt` file.

If you see a long list of credentials in your terminal, then you're on the right track! Instead of manually searching through the output, you can use a command to search for the account that corresponds to the ID you found earlier.

You can **pipe** the output of one command into another with `|`. In this case, you want to use `cat` to read the file, and then `grep` to search the output of `cat`. For example, if you wanted to search for the name "Zoe" in a file named `roster.txt`, you would run `cat roster.txt | grep Zoe`.

> [!NOTE]
>
> If you are on a Windows machine, use `findstr` instead of `grep`. For example, `cat roster.txt | findstr Zoe`.

1. Pipe `cat` into `grep` to find the username and password that corresponds to the ID you found earlier.
2. Take a screenshot of your terminal once you've found the credentials.

## Access the account

You now have the username and password of our clumsy EmptyStack engineer. It's time to access the mainframe! We'll need an administrator account to stop the project, so let's log in and look for some clues.

1. Navigate your terminal to the `emptystack` directory.
2. Run the command `node mainframe.js` to begin the login sequence. You will be prompted to enter a username and password. Enter the credentials you found earlier. If you type everything in correctly, you'll be greeted with a welcome message. If not, then run `node mainframe.js` again until you get it right.
3. Take a screenshot of your terminal once you've successfully logged in.

## Stop the project

You're in! Looks like you have some messages from an admin account. You should also have access to a list of the projects that EmptyStack Solutions is working on. You know that the codename of the project you're looking for is "LAKE".

1. Navigate your terminal to the `emptystack` directory.
2. Use your terminal to find the credentials of the admin account in `accounts.txt`.
3. Use your terminal to find the ID of project LAKE in `projects.txt`.

Once you have the admin username, password, and the project ID, you're ready to stop the project!

1. Run `node mainframe -stop` to initiate the project stop sequence. You will be prompted to enter the admin credentials and project ID. If you type everything in correctly, you'll be greeted with a congratulatory message. If not, then run `node mainframe -stop` again until you get it right.
2. Take a screenshot of your terminal once you've successfully stopped the project.

## Submission

Congrats! You have successfully stopped EmptyStack Solutions! At this point, you should feel comfortable using `pwd`, `ls`, `cd`, and `cat`. To get credit for your hard work, make sure to submit all screenshots you took during the workshop.
