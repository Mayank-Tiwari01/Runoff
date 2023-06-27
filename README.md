# Runoff
link for more info : https://cs50.harvard.edu/x/2023/psets/3/runoff/#print_winner
The program is a runoff election system implemented in C. It allows for multiple candidates and voters. Made for CS50 pset!!
The program is a runoff election system implemented in C. It allows for multiple candidates and voters. Candidates' names are provided as command-line arguments, and users can vote for their preferred candidates. The program conducts rounds of voting until a winner is determined.

The program starts by initializing the candidates with their names and setting their initial vote counts and elimination status. It also prompts for the number of voters. Each voter then submits their preferences by ranking the candidates.

The voting process is implemented in the `vote` function, which checks the validity of each vote and records the preferences accordingly. The preferences are stored in a 2D array.

To determine the winner, the program conducts multiple rounds of voting. In each round, the votes are tabulated by iterating over the preferences and counting the votes for non-eliminated candidates. The `tabulate` function updates the vote counts for each candidate.

After tabulating the votes, the program checks if a candidate has received more than half of the total votes. If so, that candidate is declared the winner using the `print_winner` function.

If no candidate has a majority, the candidate with the fewest votes is eliminated. The `find_min` function identifies the candidate(s) with the minimum votes, and the `eliminate` function marks them as eliminated.

The process continues until a winner is determined or a tie is declared. A tie occurs when all remaining candidates have the same number of votes. In such cases, the program prints the names of the tied candidates and terminates.

The program uses various helper functions to handle different aspects of the election, such as checking for invalid usage, handling maximum limits on voters and candidates, and resetting vote counts.

Overall, the program manages the runoff election process, records preferences, tabulates votes, eliminates candidates, and determines the winner based on the defined rules of the election.
