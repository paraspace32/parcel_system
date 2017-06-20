# Parcel packaging and delivery system

## Problem


We own a courier facility which segregate the courier for different cities into different racks that can hold up to &#39;n&#39; packages at any given point in time. Each level in the rack has 2 slots. The slots is given a number first to all in one column starting at 1 increasing with increasing level from the entry point in steps of one till n/2 and then to the second column as n/2+1 at the of the topmost leveldecreaseing by 1 at each lower level. We want to create an automated ticketing system that allows my facility man to use my alloted slot without any error.

Eg: if I have a rake with 10 slots, the arrangement will be like:

| 5 | 6 |
| --- | --- |
| 4 | 7 |
| 3 | 8 |
| 2 | 9 |
| 1 | 10 |



When a parcel enters my racks, we want to have a ticket issued to the parcel.

The ticket issuing process includes us documenting the parcel code and

the weight(in gm) of the parcel and allocating an available slot to the parcel before actually handing over a ticket to the facility man

(we assume that our facility men are nice enough to always park in the slots allocated to them). The Parcel should be allocated a slot which is nearest to the entry. At the exit the customer returns the ticket which

then marks the slot they were using as being available.



Due to government regulation, the system should provide me with the ability to find out:



a) Parcel codes of all parcels of a particular weight.

b) Slot number in which a parcel with a given code is parked.

c) Slot numbers of all slots where aparcel of a particular weightis parked.



We interact with the system via a simple set of commands which produce a specific output. Please take a look at the example below, which includes

all the commands you need to support - they&#39;re self explanatory. The system

should allow input in two ways. Just to clarify, the same codebase should support both modes of input - we don&#39;t want two distinct submissions.



1) It should provide us with an interactive command prompt based shell where commands can be typed in

2) It should accept a filename as a parameter at the command prompt and read the commands from that file

\*Example: File\*

To run the program:

$ my\_program file\_inputs.txt &gt; output.txt



## Input (in file):

create\_parcel\_slot\_lot 6



park 1234 400 park 9999 400 park 0001 600 park 7777 100 park 2701 700 park 3141 600

leave 5 for delivery status

park 333 400

park 9999 400 parcel\_code\_for\_parcels\_with\_weight400 slot\_numbers\_for\_parcels\_with\_weight400 slot\_number\_for\_registration\_number3141 slot\_number\_for\_registration\_number1111



## Output (to console, new line after every output):

Created a parcel slot with 6 slots

Allocated slot number: 1

Allocated slot number: 6

Allocated slot number: 2

Allocated slot number: 5

Allocated slot number: 3

Allocated slot number: 4

Slot number 5 is free

Slot No. Registration No.   Weight

| 1 1234 | 400 |
| --- | --- |
| 6 9999 | 400 |
| 6 0001 | 600 |
| 3 2701 | 700 |
| 4 3141 | 600 |

Allocated slot number: 5

Sorry, parcel slot is full

1234, 9999, 333



1, 6, 5

4

Not found
