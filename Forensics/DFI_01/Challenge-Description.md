# Abdullah Ali Alhakami
# Twitter : @Alhakami1_
# Email : Aalhakami.26@gmail.com

Description : Show me your skills in volatility . 

Level : Easy

Enjoy : 


First let’s check the process was running using volatility2 , and plugin pslist .
Command : vol.py -f mem01.raw --profile=Win7SP1x64 pslist

![image](https://user-images.githubusercontent.com/99384019/153737005-da540fcf-7731-427a-a9b9-5e29d77ab56a.png)

The firefox web browser was running , so let’s check the history to know the sites the suspect visited . Using iehistory plugin .
Command : vol.py -f mem01.raw --profile=Win7SP1x64 iehistory

![image](https://user-images.githubusercontent.com/99384019/153736574-9ea01319-754d-4f26-a837-d5256b0240bc.png)

While analyzing the history we notes there is a suspicious link related to pastebin . Let's see what the site contains 

![image](https://user-images.githubusercontent.com/99384019/153736583-e98e6980-f9f3-4d9d-8828-cf2f48e8ae86.png)
 
Woow . What is the password ? let’s go check the the files on the memory dump using filescan plugin 
Command : vol.py -f mem01.raw --profile=Win7SP1x64 filescan | grep password -i

![image](https://user-images.githubusercontent.com/99384019/153736591-a24d6cb8-7ae9-4150-96de-d167577cff82.png)
 
Hmm , let’s dump it using dumpfiles -Q <Offset(P)> -D /Output/

We found interesting password in that file ? 

![image](https://user-images.githubusercontent.com/99384019/153736606-8a187bca-3919-4a5a-b1aa-0ce4ae298afb.png)

But wait  , that doesn't make any sense, it's definitely encrypted
Using CyberChef “magic operation” we found the password : 
Notes : Delete the lines .

![image](https://user-images.githubusercontent.com/99384019/153736624-2efa127a-1ef1-4375-a8d7-b7dc03c39070.png) 

Now let’s use the password in https://pastebin.com/dvtPt6T7 

![image](https://user-images.githubusercontent.com/99384019/153736633-4b11813d-d478-4bc5-b41f-f66f2f0b8bef.png)

Flag : cyberhub_{easier_that_i_thought!memory_master}

