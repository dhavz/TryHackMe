# Overpass 2 - Hacked
----------------------------------------

## [Task 1] Forensics - Analyse the PCAP

1 	What was the URL of the page they used to upload a reverse shell? <br>
2 	What payload did the attacker use to gain access? <br>
3 	What password did the attacker use to privesc? <br>
4 	How did the attacker establish persistence? <br>
5   Using the fasttrack wordlist, how many of the system passwords were crackable? <br>

For task 1 analyze the pcap file using any tool like wireshark. Look HTTP streams you will get your answers. <br>


## [Task 2] Research - Analyse the code

Now that you've found the code for the backdoor, it's time to analyse it. <br>
1 	What's the default hash for the backdoor? <br> 
2 	What's the hardcoded salt for the backdoor? <br>
3 	What was the hash that the attacker used? - go back to the PCAP for this! <br>
4 	Crack the hash using rockyou and a cracking tool of your choice. What's the password? <br>
<br>
For Q1 and Q2 answer you will get one intresting URL from the Pcap. That url points to some kind of backdoor. There you will find this answers. <br>
For Q3 You will get that in PCAP only <br> 
For Q4 I like to use hashcat: hashcat -a 0 -m [MOD] hash /usr/share/wordlists/rockyou.txt <br>

## [Task 3] Attack - Get back in!

Now that the incident is investigated, Paradox needs someone to take control of the Overpass production server again. <br>

There's flags on the box that Overpass can't afford to lose by formatting the server!  <br>
1 	The attacker defaced the website. What message did they leave as a heading? <br>
Export HTTP Objects you will get the Ans other wise Deploy the machine and get the answer <br>

2 	Using the information you've found previously, hack your way back in!  <br>

3   What's the user flag? <br>
Time to use the deployed backdoor. <br>
Backdoor pointing to some port. <br>

ssh user@BOXIP -p [Intresting Port] <br>
user - pcap is helpfull
password you already cracked it. <br>

cat user/user.txt <br>

You can have user flag. <br>

4   What's the root flag? <br>
There is one intresting binary(s****_*ash) available under user. use that with -p You will have root access. <br>

cat /root/root.txt <br>
will get the root falg. <br>

Go Go get the flags.

