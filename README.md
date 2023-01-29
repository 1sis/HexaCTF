
# <u>The Lawyer</u> :

**<u>Resume</u> :**
In this CTF, we investigate "Nelexat" a Swiss legal company created especially for this event. For that, several points allow us to find the totality of their actions towards "Lucilhe", their customer.

![Survey_TheLawyer](./Survey_TheLawyer/Survey_TheLawyer.png)


# <u>The law firm</u> :

## <u>Statement</u>
![Statement_The-Law-Firm.png](./Survey_TheLawyer/The-Law-Firm/Statement_The-Law-Firm.png)
-  We understand that "Nelexat" is a Swiss law firm defending "Lucilhe". We also note that they have a website.
-  The Swiss extensions of the site are ".ch" so we find the link: "http://www.nelexat.ch/"
-  We just have to read the flag in the footer of the site

 **FLAG : HEXA{N3l3x4t_w1ll_M4ke_You_R1ch}**

![Footer_flag](./Survey_TheLawyer/The-Law-Firm/Footer_Nelexat.png)

# <u>Trustwhorty</u> :

## <u>Statement</u>
![Statement_TrustWhorty](./Survey_TheLawyer/Trustworthy/Statement_Trustworthy.png)

**[Unlocked after completing "The Law Firm"]**

-  In this situation, the title puts us in the way of "confidence". Looking at the URL, we see that the connection is not secure. Then we just have to look at the certificate information to find the email "mastermind_mastermind@proton.me"

**FLAG : HEXA{mastermind_mastermind@proton.me}**

# <u>The lawyer</u> :

## <u>Statement</u>
![Statement_The-Lawyer.png](./Survey_TheLawyer/The-Lawyer/Statement_The-Lawyer.png)

**[Unlocked after completing "The Law Firm"]**

-  Here we need to search in which city studied the owner of the company. Nothing more simple, we search a little on their website. A name is given in the legal conditions: "Lian Nussbaumer"

![Search_Lian-Nussbaumer.png](./Survey_TheLawyer/The-Lawyer/Search_Lian-Nussbaumer.png)

-  By searching his name on Linkedin, a profile exists with this name: https://www.linkedin.com/in/lian-nussbaumer-92b89b253/

![Footer_flag](./Survey_TheLawyer/The-Lawyer/Linkedin_Lian-Nussbaumer.png)


-  He is the owner of the company and we find that he studied in the city of **"Neuchâtel"**.

 **FLAG : HEXA{Neuchatel}**

# <u>Experts</u> :

## <u>Statement</u>
![Statement_Experts](./Survey_TheLawyer/Experts/Statement_Experts.png)

**[Unlocked after completing "The Lawyer"]**

- For this one, we need to look for information around the Nelexat company's customer. To start, we find an API host on an external IP hidden in their tips page:

![FastAPI_Experts](./Survey_TheLawyer/Experts/FastAPI_Experts.png)

- FastAPI proposes an endpoint "/docs/" which will be useful for the following.
We understand that we have to search for the client's last name. 
At the very beginning of the CTF, the organizers made a voice explaining that it happened the previous year, which allowed us to have the last name of Lucilhe.

- Coupling all this information, we test the endpoint "http://217.182.69.14:8000/cases/clients?name=dumarquais" and we find the flag !

![Flag_Experts](./Survey_TheLawyer/Experts/Flag_Experts.png)

**FLAG : HEXA{s3cure_y0ur_d4mn_4p1}**

# <u>Alias</u> :

## <u>Statement</u>
![Statement_Alias](./Survey_TheLawyer/Alias/Statement_Alias.png)

**[Unlocked after completing "The Lawyer"]**

-  For this challenge, we must find his account on a trading platform. While viewing Lian's posts, we find a rather interesting post for the next part:

![Post_Lian-Nussbaumer.png](./Survey_TheLawyer/Alias/Post_Lian-Nussbaumer.png) 
-  We now have his nickname: **"NelexLian"**.
-  Searching on Etoro (known trading platform) we find a user "NelexLian" with the flag on his profile!

![Etoro_NelexLian](./Survey_TheLawyer/Alias/Etoro.png)

**FLAG : HEXA{nelexlian_is_rich}**

# <u>Herbaceous</u> :

## <u>Statement</u>
![Statement_Herbaceous](./Survey_TheLawyer/Herbaceous/Statement_Herbaceous.png)

**[Unlocked after completing "Trustwhorty"]**

- Using the email address "mastermind_mastermind@proton.me" on https://epieos.com, we find a calendar linked to a google account.

![Calendar_Herbaceous](./Survey_TheLawyer/Herbaceous/Calendar_Herbaceous.png)

- Reading the event "meeting" we find a link in ".onion". After	 an express copy and paste on Tor (and a taped camera because TheBaboon likes to see you smile), we just have to inspect the page to find the flag! We will take the wallet address information used in the following challenges.

![Web_onion_Herbaceous](./Survey_TheLawyer/Herbaceous/Website_onion_Herbaceous.png)

**FLAG : HEXA{N3l3x4t_is_L1nk3d_to_M4stermind}**

# <u>Decentralised</u> :

## <u>Statement</u>
![Statement_Decentralised](./Survey_TheLawyer/Decentralised/Statement_Decentralised.png)

**[Unlocked after completing "Herbaceous"]**

- Using the wallet address found earlier, we search on "https://blockchain.com" to find the transaction history. 

![transaction_decentralised](./Survey_TheLawyer/Decentralised/transaction_decentralised.png)

- Looking at the 1st one, we have data transferred with "636f6e74616374206d61696c203a20747375796f36334070726f746f6e2e6d650d0a636f6465206e616d65203a204272756973656420526f677565"

![Data_decentralised](./Survey_TheLawyer/Decentralised/data_decentralised.png)

- decoded in hexadecimal, we find the name of the mission and an email address :D

![Decoded_hexa_Decentralised](./Survey_TheLawyer/Decentralised/decoded_hexa_decentralised.png)

**FLAG : HEXA{Bruised_Rogue}**

# <u>Good time</u> :

## <u>Statement</u>
![Statement_Good-time](./Survey_TheLawyer/Good-time/Statement_Good-time.png)

**[Unlocked after completing "Herbaceous"]**

- For this challenge, let's use the same methodology as Herbaceous: the meeting.
 If you are connected to a Google account and look at the calendar, you will see the mails of the concerned persons.

![Mails_good-time](./Survey_TheLawyer/Good-time/Mails_good-time.png)

- Knowing this, we can see two mails. Epieos not giving anything, we look for the nicknames on "https://whatsmyname.app" 

![whatsmyname_good-time](./Survey_TheLawyer/Good-time/whatsmyname_good-time.png)

- and we find a Tripadvisor giving the location of the meeting :p

![tripadvisor_good-time](./Survey_TheLawyer/Good-time/tripadvisor_good-time.png)

**FLAG : HEXA{Kaufleuten}**

# <u>Kanagawa</u> :

## <u>Statement</u>
![Statement_Kanagawa](./Survey_TheLawyer/Kanagawa/Statement_Kanagawa.png)

**[Unlocked after completing "Decentralised"]**

- With the wallet address we found in "Herbaceous" we just had to look for a way to receive money other than through simple transactions.

- Opensea is a way to sell NFTs which seemed most likely. Typing in the address, we came across an account named  (Mind_master) selling an NFT. 

![Opensea_Kanagawa](./Survey_TheLawyer/Kanagawa/Opensea_Kanagawa.png)

- Searching in the description, we find the flag :)

![Flag_Kanagawa](./Survey_TheLawyer/Kanagawa/Flag_Kanagawa.png)

**FLAG : HEXA{n1ce_L0g0_br0}**
