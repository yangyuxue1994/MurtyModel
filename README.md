# Episodic Memory Model for Value-based Decision-making

### Main idea

PSS study indicated that we make decisions based on the sense of good vs. bad, and how good it is vs. how bad it is, by learning the probability associated with each option. But this paradigm does not allow Pps to form SPECIFIC and DETAILED outcome(how good?) associated with each option.
**![](https://lh5.googleusercontent.com/UbOot2fvhi3ch05IUPrS4h3zSz93-AIcBW-YZ9QYmaeNJv2TAOXB83JPV4Q7nhjrnaDivD9AQFd22dakdcKYxrT8VvYaFURNxpc4DNjnN0Xc16yHE5FP19hnKOAdS6SU1dqXrs65)**
People rely on prior experience to make decisions. This requires memories to be retrieved and displayed when making decisions. Past studies have been focusing on the effects of procedural and WM on value-based choices. (E.g. Larger capacity of WM/ Better executive function is associated with greater willingness to work for larger rewards. etc.) Interestingly, Murty (2016)’s study showed that one single episodic memory(event memory) can also affect value-based decision making process.

This model will help us to understand how episodic memory influence value-based choice. How are these memories accessed during choices? This also provides insights in understanding reward representation (positive vs. negative AND high vs. low).



### Experiment 1

 - TASK1: Reward Task
		 - Pps played 60 trials of game involving 60 lotteries 
		 - See a unique image of house, and amount of money given by this house 
		 - low value ($0.1-$1.5) vs. high value($3.5-$5)
- TASK2: Distractor Task
		- Pps completed math problems (no feedback)
- TASK3: Decision Task
		- Pps saw 2 house stimuli representing 2 lotteries, and they had to decide which lottery they would prefer to play
		- Line-drawing house (random) vs. Encountered house/novel house
- TASK3: Memory Task
		- Pps saw a picture of house, and they had to indicate whether they had seen this with a confidence level(1 high confidence old -5 high confidence new)
		- If responded with 1,2,3, they were asked how much money was associated with house's outcome(0-5)
**![](https://lh4.googleusercontent.com/Rkov1IFxe8XHeIlXE_cj4ti3skMvZfVKwdVWcpqk1r987lp60B_Tq-r2Q1F5P5aGF8w3jwRift9CaWxF9ZjL_8UHutvg41S7ztOZdzATAUv5IjikeOFVD5qX8xbN4gYYRMv7ywqU)**
### Results
- PPs reported positive feeling about high value lotteries
- PPs selected lotteries more often when they had been previously associated with larger values --> use prior experience to guid behaviors
- When PPs remembered both lottery stimulus and the associated value, they choose high lotteries more often. 

### Summary
-   People were able to use specific, accurate details (which specific house is associated with how much money), to choose adaptively in subsequent decision-making task, selecting stimuli previously associated with higher rewards.
    
-   Item memory (remember whether you have encountered the house stimuli or not) does not contribute to adaptive choice

### ACT-R Model Design
This model is using PyACTUP module, a ACT-R package in Python.
Pseudocode (2020/01) 
T0
Reward Task:
- Present Stimulus1 (House1) + Value1 ($4.9)
- Encode as 2 separate chunks in LTM
- Retrieve feelings: Low vs. High (prior knowledge)
	- $.1-$2.5 - Low
	- $2.6-$5 - High
Distraction task: 
Decision task: 
- Present 2 stimuli, house1 vs. line draw house (house0)
- Retrieve house1,
	- If success, then retrieve category associated with house1
		- If success:
			- If in high category THEN (select it)
			- If in low category THEN (select line draw house, house0)
		- Else: Randomly select either house 1/house0
	- Else: Randomly select either house 1/house0
T2
Memory test:
- Present house1 stimulus
- Retrieve house1,
	- If success, Respond yes
	- Else, Respond no

NOTE: in this case, ACTR always remember every stimulus. Can we simulate the forgetting? Do we need to do so?
	- Use activation threshold 

- Given house1, retrieve the associated value
	- If success, report amount
	- Else, Respond no

### PyACTUP Model
todo...
 
 
