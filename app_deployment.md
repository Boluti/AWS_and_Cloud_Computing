
## Prerequisite ## 
## Steps in creating an instance ##

1. Name_and_tags:  use tech254_bolutife_nginx
![img_2](https://github.com/Boluti/AWS_and_Cloud_Computing/assets/145682024/7bcecf65-3fcc-46e6-a77e-82927f98a25b)

2. Application and OS images: Browse more AMIs, Community AMIs, then search , select ubuntu from the two options

3. Instance type: choose t2.micro( resources being used)18.04 lts 1e9
4. Key pair login : use tech254
5. ensure the .pen file is on .ssh folder
6. Edit security group under network settings. change security group name to tech254_bolutife_basesg
![img_3](https://github.com/Boluti/AWS_and_Cloud_Computing/assets/145682024/16fe5260-7f35-4115-a74b-8270c6793f3d)

Copy the same thing to the description group.
![img_4](https://github.com/Boluti/AWS_and_Cloud_Computing/assets/145682024/6323b495-2682-4fd6-bc12-f7d38c40861e)

7. Inbound security group rules; select ssh for the first one; and source type being anywhere
8. Add security group rule. Under the security group rule, choose HTTP; source type anywhere.
9. Security group rule 3: Add HTTPS; source type: anywhere. 
 ![img_6](https://github.com/Boluti/AWS_and_Cloud_Computing/assets/145682024/7202a12a-63ef-4743-8551-d2e5df25cd5f)

10. Configure storage: no change required. 
11. Select launch an instance. Under instance summary, copy public ip address
![img_8](https://github.com/Boluti/AWS_and_Cloud_Computing/assets/145682024/4d537d0d-1c2a-4c29-a6ed-efa3bf9eb010)

12. Instance summary page

13. Add a third security group. Add rule > Custom TCP. Port range = 3000. Source = Anywhere-IPv4. Save rules. 

# Connecting to instance on Gitbash 
$ `cd  .ssh/` : Run command to take you inside ssh folder. 

$ `chmod 400 tech254.pem` 

$  `ssh -i "tech254.pem" ubuntu@ec2-34-244-68-150.eu-west-1.compute.amazonaws.com`

$ git clone https:github.com/LSF970/sparta_test_app.git
- Do the following: 
`$ ls` : run command to see if app is in there
 then `$cd Sparta_test_app` then `$cd app` to go into the app folder. 

# Make sure your machine is up to date.
- `sudo apt update 
The above command searches and files the available updates for your machine, but does not install and deploy them.

- `sudo apt upgrade -y`
The above command deploys the changes from the previously cached downloads.

The `-y` flag agrees to all changes automatically.
Do this step before launching important applications, as later updates and upgrades may cause issues

## Setting up NodeJs.
For this particular application, an older version of NodeJs is required to run it. For more modern applications, use the applicable command to download the NodeJs version required.

- `curl -sL https://deb.nodesource.com/setup_12.x | sudo -E bash -`
This command notifies the system that when downloading NodeJs, this is the package to use.
Following this, run the following command:

`sudo apt install nodejs -y`: Now, run the command:
![img_15](https://github.com/Boluti/AWS_and_Cloud_Computing/assets/145682024/ff9f5d96-1496-480e-a19d-96a12d496f88)

`sudo npm install pm2 -g`: This is now using the Node Package Manager to install dependencies.

## Final installation command:

- Make sure to cd into the necessary app folder for this command:
- `npm install`: This command installs all libraries located within the environment required to run the file.
While in this file, run the final command:

`node app.js` 

![img_16](https://github.com/Boluti/AWS_and_Cloud_Computing/assets/145682024/6201c71a-9593-420d-9583-6d3608dfea65)

 ![Uploading img_17.png…]()
