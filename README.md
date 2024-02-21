
# Is this for me?

If you are looking to deploy your nodejs script/discord bot to cloud and want it to run 24/7 but not sure how to do it, you are in the right place.




## Requirements

You need to have a vps where you could run the scripts. The Ip address, port and password is enough.
## Lets start

The steps are pretty easy. This guide is made on assumption you have read my general guide. If not, [here](https://github.com/bilal-the-dev/How-to-run-my-discord-bots). That will be needed in future. Enough talk, more action now:

- Open `command prompt`
- Type `ssh root@[ip address here]` .e.g `ssh root@207.240.89.50` where root can vary, its the username.
    - If this gives you error then you need to add your port as well `ssh -p 5809 root@207.240.89.50`
- It'll ask for password, after entering type `Yes` to save the host.
![vps](https://cdn.writebots.com/wp-content/uploads/2022/02/img_61ff06abf3934.png.webp)
Great VPS is opened now!
## Installing dependencies

Run the following cmds one by one.

```bash
sudo apt update
sudo apt install git
sudo apt install nodejs
sudo apt install npm
npm install -g pm2
```
As name say, they are for installing node js and other.

We are using `pm2` here, although i love to use **docker** thats not beginner friendly tho.

 Now check the version of nodejs using `node -v` if its less than **16** then run following commands

```bash
sudo npm install -g n
sudo n stable
hash -r
```

Great, we are close to running our bot.

Import the repo by cloning it, you can refer to the installation section on my general guide.Follow the environment variable and config section as well.

Few steps ahead,
 -  Enter the directory using `cd [folder name]`
 - Run `npm install`
 -  Run `pm2 start index.js --name "myDiscordBot"` and boom its on!
 ![vps](https://cdn.writebots.com/wp-content/uploads/2022/02/img_61ff0ad607fb1.png.webp)

 You can close the terminal and bot will still work :D

If you face any problem, please open a issue.
