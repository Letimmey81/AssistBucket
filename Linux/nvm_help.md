`nvm list`

If the data: "default" is similar to "default -> lts (-> N/A)"

You have the same problem as I had, let's solve it by doing the following:

After installing nvm, run the command: "nvm install node --lts" without the quotes!

If everything goes well, it will display something like:

Installing latest LTS version. Now using node v18.18.0 (npm v10.1.0)

In my case, note that the exact installed version of lts was "v18.18.0" you need to set a default version otherwise, running the nvm list command you will see that the nvm default will be set to N/A

If after running the "nvm list" command you notice that the "default" parameter is:

`default -> lts (-> N/A)`

It means that the default version for use has not been defined, which is why you can run nvm in the terminal, but you cannot run npm or node -v

So finally, resolve this by setting the default version for NVM:

Run: "nvm list" and see if it appears in the list: "lts/hydrogen -> v18.18.0"

Now run: "nvm alias default lts/hydrogen" If ok, it will display the message: "default -> lts/hydrogen (-> v18.18.0)"

Finish with the command: "nvm use default" If ok, it will display the message: "Now using node v18.18.0 (npm v10.1.0)"

Checking before and after running the "nvm list" command

Before: default -> lts (-> N/A)

After: default -> lts/hydrogen (-> v18.18.0)
