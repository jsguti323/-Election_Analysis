# Election_Analysis

## Project Overview
A Colordado Board of Elections has given you the following tasks to complete the elections audit of the recent local congressional election:

1. Calcilate the total number of votes cast.
2. Get a complete lst of candidate who received votes.
3. Calcuate the total number of votes each candidate received.
4. Calculate the percentage of votes each candidate won.
5. Determine the winner of the election based on popular vote.

## Resources
- Data Source: election_results.csv
- Software: Python 3.6.1 , Visual Studio Code, 1.38.1

## Election Audit Results
The analysis of the election shows that:
- There were 369,711 votes cast in the election.
- The candidates were:
  - Diana DeGette
  - Charles Casper Stockham
  - Raymon Anthony Doane
- The counties voting in the election were:
  - Jefferson
  - Denver
  - Arapahoe
- county voting results were:
  - Jefferson: 10.5% of the total votes (38,855).
  - Denver: 82.8% of the total votes (306,055).
  - Arapahoe: 6.7% of the total votes (24,801).
- The county with the biggest voter turnout was:
  - Denver
- The candidate results were:
  - Diana DeGette won 73.8% of the votes with 272,892 total votes.
  - Charles Casper Stockham won 23.0% of the votes with 85,213 total votes.
  - Raymon Anthony Doane won 3.1% of the votes with 11,606 total votes.
- The winner of the election was:
  - Dianna Degette, who received 73.8% of the votes with 272,892 total votes.

## Summary
- with open(file_to_load) as election_data:
  - reader = csv.reader(election_data)
  - header = next(reader)
  - for row in reader:
    
All this code is telling the computer to do is read the csv file, pull relevant data, and count that data. Once that data is counted, it's placed in either a list or dictionary we counted. Two examples are:

- county_list = []
- county_votes = {}

These data stores are two of the features of this code specific to this election. The former is a list holding all of the names of the different counties that had submitted votes in the election. The latter is a dictionary containing both the names of the counties involved, as well as the number of votes that came out of each county. Elections can vary in size, however, and while this election counted votes from the counties, you could have a smaller, city wide election, or even a larger, nation wide election. So if you choose to use this code for future elections, please be mindful of that when choosing the names of your lists and dictionaries. A list of states voting in a national election named "county_list" can be very misleading.

The only other example I can find in the code that could use some modifying is:

- county_total = county_votes.get(county_name)

Personally I would just do:

- county_total = county_votes[county_name]

It has the same output and it makes the code a little more consistent and clean.

Other than that, I hope you find this analysis useful!