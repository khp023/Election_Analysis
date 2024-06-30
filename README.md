# Election Analysis Project

## Overview of Sample Election Audit

In this scenario, the Colorado Board of Elections had an initiative to perform an audit of the results of a local congressional election. The data is provided by UCSD's Data Science with edX, as provided in [election_results.csv](Resources/election_results.csv). Despite this data being relatively small in size and digestible through Excel, Python was chosen as the appropriate tool to not only automate but also set up the framework for scalability for future election runs. Key statistics obtained from this study include: 

1. Total number of votes cast in the election. 
2. A list of candidates involved with their results (voter count and percentage)
3. The winner of the popular vote. 
4. County participation and identification of the county with the best turnout 

As developed in [PyPoll_Challenge.py](PyPoll_Challenge.py), the success of the analysis will be determined through the usage of lists, dictionaries, and interative loops to filter the information.


## Sample Election Audit Results 

Final results were outputted not only in the terminal through `print()` methods but also saved to an external .txt file. Having declared `file_to_save` as the variable representing output file [election_analysis.txt](/Analysis/election_analysis.txt), we used `with open(file_to_save, "w") as txt_file:` to initiate saving the file with `txt_file.write()` as the tool to print lines in the file. 

Below is a screenshot of [election_analysis.txt](/Analysis/election_analysis.txt) showing the full results.

![election_analysis.txt](/screenshots/analysis.png)

The results show the outcomes for the counties Jefferson, Denver, and Arapahoe; with the outcomes for candidates Charles Casper Stockham, Diana DeGette, and Raymon Anthony Doane. Additionally we find the following: 
- Diana DeGette was the overall winner with the winning popular vote total of 272,892- receiving 73.8% of the total 369.711 votes cast
- Denver County had the largest voter turnout at 306,055, being 82.8% of the total 369.711 votes cast

## Sample Election Audit Summary

The code performed successfully in giving the results that the audit required. The importance of this data exploration is that it is not bound to this exact database file. Simply, in the event that the database has different columns, the lists can be adapted easily as seen in line 49 `candidate_name = row[2]`. The usage of for loops to iteratively add information to these lists and dictionaries eliminates absolute values such that it can be applied in future elections.

As identified prior, Diana DeGette and Denver County's election percentages are in the supermajority range being so high. Additional statistics that may be useful would be the percentage of votes that a particular candidate received from each county. The inverse would be useful too - determining each county's percentage split that the constituents voted for. Data exploration can be leveraged for statistics to lead into visualizations and charts that could be useful for campaign teams. 

An additional exercise in showing the process through a pandas jupyter notebook in parallel is added in [PyPoll_pandas.ipynb](PyPoll_pandas.ipynb)

## Resources
- [election_results.csv](Resources/election_results.csv) as provided by UCSD Data Science and Visualization program