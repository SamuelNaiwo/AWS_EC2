# Set Up A EC2 Instance

1. Login on the AWS website.

![1. AWS Log In.png](img%2F1.%20AWS%20Log%20In.png)

2. Using the search bar at the top, search 'EC2' and click EC2 (Virtual Servers in the Cloud)

![2. Search EC2.png](img%2F2.%20Search%20EC2.png)

3. Select the Instances (running) button.

![3. Instances (running).png](img%2F3.%20Instances%20%28running%29.png)

4. On the far right hand side, click Launch Instances and select launch instances.

![4. Launch instances.png](img%2F4.%20Launch%20instances.png)

5. Title your instance.

![5. Name convention.png](img%2F5.%20Name%20convention.png)

6. Select Browse more AMIs to show you more options.

![6. Browse More AMIs.png](img%2F6.%20Browse%20More%20AMIs.png)

7. Select the server that you want. Leave it at default which should be 64-bit (x86)

![7. Ubuntu Server.png](img%2F7.%20Ubuntu%20Server.png)

8. Select the instance type which fits best.

![instance type.png](img%2Finstance%20type.png)

9. Select your key pair name. You can create one if you don't have already.

![key pair login.png](img%2Fkey%20pair%20login.png)

10. Scroll down to network settings and change 'Allow SSH traffic from' to 'MY IP'. Also select 'Allow HTTP traffic from the internet'

![8. Network setting.png](img%2F8.%20Network%20setting.png)

11. Select edit in Network settings and create your security group name. Copy that name and paste underneath in the description.

![security group.png](img%2Fsecurity%20group.png)

12. When you launch your new instance, this will box will show if you're successful. Click the 

![10. Successful launch.png](img%2F10.%20Successful%20launch.png)

13. Under the status check tab, check to see if you have 2/2 checks passed.

![12. Click connect .png](img%2F12.%20Click%20connect%20.png)

14. Click connect at the top of the page.

![12. Click connect .png](img%2F12.%20Click%20connect%20.png)

15. Open your terminal/bash window.

![13. Open terminal:bash.png](img%2F13.%20Open%20terminal%3Abash.png)

16. Change directory into your .ssh folder where your ssh key should be stored. Use the command below

```commandline
cd .ssh
```

![14. cd to .ssh folder.png](img%2F14.%20cd%20to%20.ssh%20folder.png)

17. Copy your chmod command and paste into terminal/bash to ensure key is not publicly viewable

![15. copy chmod.png](img%2F15.%20copy%20chmod.png)
![16. chmod command.png](img%2F16.%20chmod%20command.png)

18. Copy your ssh key and paste into terminal/bash. Type yes if it asks you 'Are you sure you want to continue connecting?'

![17. copy ssh key.png](img%2F17.%20copy%20ssh%20key.png)
![18. Click yes .png](img%2F18.%20Click%20yes%20.png)
![19. Success.png](img%2F19.%20Success.png)

19. Once your in ubuntu, run this command below to update.

```commandline
sudo apt update
```

![18. sudo apt update.png](img%2F18.%20sudo%20apt%20update.png)

20. After running an update, run this command below to download the update.

```commandline
sudo apt upgrade
```

![19. sudo apt upgrade.png](img%2F19.%20sudo%20apt%20upgrade.png)

21. To install nginx run this command below. We use `-y` at the end of the command to skip the confirmation.

```commandline
sudo apt install nginx -y
```

![20. sudo apt install nginx -y.png](img%2F20.%20sudo%20apt%20install%20nginx%20-y.png)

22. We then check to the status and making sure everything is running with the below command.

```commandline
sudo systemctl status nginx
```

![21. sudo systemctl status nginx.png](img%2F21.%20sudo%20systemctl%20status%20nginx.png)

23. Copy our public IPv4 address and paste it into a new window in your internet browser.

![22. public ipv4 address.png](img%2F22.%20public%20ipv4%20address.png)

24. You will see this and you have completed your set up.

![welcome to nginx.png](img%2Fwelcome%20to%20nginx.png)