# Abdullah Ali Alhakami
# Twitter : @Alhakami1_
# Email : Aalhakami.26@gmail.com

Description : Our server under attack , what is going on ?

Level : Hard

Enjoy :


First let's open the log file with notepad : 

![image](https://user-images.githubusercontent.com/99384019/153737696-2bf04c35-8a12-4baf-bf75-000248207e0a.png)

There is GET request and base64 encoded code ?  So let’s decode it simply .

![image](https://user-images.githubusercontent.com/99384019/153737698-f2fa2d30-53e7-4b10-994b-58faa0b3c3d8.png)
 
This is blind SQL injection attack , we use a script to get the flag , to know how the attack works: https://var3d.tistory.com/164

![image](https://user-images.githubusercontent.com/99384019/153737711-4f0dd59b-6fa3-488b-8735-badb136b4d45.png)

Now let’s run the script on the log file

Flag : g9UWD8EZgBhBpc4nTSAS
