Description : ... Mirror 

Level : Easy

Enjoy :

@Alhakami

First let's open the PCAP files using wireshirk : 
While analyzing the packets on tcp protocol , we notes there is only one packet have a data : 

![image](https://user-images.githubusercontent.com/99384019/153739288-45dcefcf-17b1-454a-a250-f8ea043b2a78.png)

![image](https://user-images.githubusercontent.com/99384019/153739304-dc714efe-448d-4189-a5ad-45bce8b1be28.png)


Wait , What is FIFJ !!! maybe that’s mean an image (Because jpeg images contain JFIF on her header)? but wait it supposed to be JFIF . 
Okay but remember the hint in the challenge he says it’s a mirror . So if we reverse the FIFJ it will be JFIF . 
So we will dump the data and reverse it using cyberchef . 
 
 ![image](https://user-images.githubusercontent.com/99384019/153739317-27c86252-18bd-4d08-b7f9-dda731616e88.png)


Let’s save it and see the picture : 
 
 ![image](https://user-images.githubusercontent.com/99384019/153739321-786ddd1e-e457-4431-a6e8-a1ef86a6c93a.png)


Flag : cyberhub_{ba71f5ad35cb194dbc744c360557109b}

:>
