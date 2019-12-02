GROUP DETAILS:
Krithika.J.   1KS17CS036
Meghana.G.    1KS17CS042
Meghana.G.R.  1KS17CS043

DESCRIPTION:
According to our question A08, USN: 1KS17CS036 which is the lowest USN.According to the question we have to do the following operation X=D+10=> X=6+10=16 and Y=X/2=>16/2=8
So,we have X=16 which is the number of packets and Y=8 which is the burst value 

RULES:
Rule 1: sudo iptables -I OUTPUT -d 192.168.43.177 -p icmp --icmp-type 8 -m limit --limit 16/minute --limit-burst 8 -j ACCEPT
RULE 2: sudo iptables -A OUTPUT -d 192.168.43.177 -p icmp --icmp-type 8 -j DROP
ping -c 60 192.168.43.177

HOW IT WORKS:
As we have given the burst-limit to be 8 it will send packets upto 10 the extra 2 are because of the average value and another start value.
As we have given the limit to be 16, 16packets will be sent per minute.
We have used --icmp-type 8 as 8 indicates request (icmp:Internet Control Message Protocol).
The ACCEPT function accepts the connection on socket
-A, --append chain rule-specification Append one or more rules to the end of the selected chain.  When the  source  and/or  destination  names resolve to more than one address, a rule will be added for each possible address combination.
-I, --insert chain [rulenum] rule-specification insert one or more rules in the selected chain as the given rule number.

CHALLENGES FACED:
The main cahllenges faced was with the syntax errors 
As we did not have virtual box it was difficult to do the assignment
We were not clear with getting the wireshark capture as we did not know to use wireshark properly
