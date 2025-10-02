# PrimeX

This software project accompanies the research paper, [PrimeX: A dataset of worldview, opinion, and explanation](https://arxiv.org/abs/2510.00174).

Public opinion survey data from a diverse set of 858 American participants with two novel sources of additional information: written explanations from the respondents for why they hold specific beliefs, and the 18 question Primal World Belief instrument for assessing worldview.

## Documentation

The PrimeX dataset is in `primexdata.csv`. This file has the following format:

- Row 1: Column Titles
- Row 2 - 859: Per-user responses 

Considering the columns, there are some features to note:
- Pew Research Survey Questions: Columns 28, 34, 40, 46, 47, 48, 49, 50, 51, 52, 53, 59, 65, 71, 72, 73, 74, 75, 76, 77, 78, 84, 90, 96, 97, 98, 99, 100, 101, and 102
- Explanations for previous opinion: Columns 29, 35, 41, 54, 60, 66, 79, 85, 91
- Primal World Beliefs survey questions: Columns 103, 104, 105, 106, 107, 108, 109, 110, 111, 112, 113, 114, 115, 116, 117, 119, 120, and 121
- Column 1: Unique Identity for each respondent 
- Column titles beginning with "Timing" record various features of the time each respondent spent on different pages of the survey. 
- There are two attention checks in this data: Column 16 corresponding to "Hobbies - Soap Carving" and Column 118, an attention check in the Primal World Belief Survey. Disregard the responses from these columns. 
- Remaining columns cover self-identified demographic attributes of respondents: geographic region, age range, gender, English proficiency, number of children, employment status, political affiliation, hobbies, other languages spoken at home, religious affiliation, and races.


Additional metadata is available in `metadata.json`. This json has the following fields:
- 'opinion\_questions': indices of Pew Opinion Questions in `primexdata.csv`
- 'questions\_with\_explanations': list of pairs of indices pointing to opinion questions and their explanations. Each item has a `question` and `explanation` field. 
- 'PI-18': list of indices of PI-18 items, each associated with the question code for scoring (see Appendix C for scoring details). Each item has a `index` and `code` field.
- 'demographic\_questions': indicies of demographic questions.
- 'test\_identities': list of user Identities (column 1) for test split used in paper. 


## License

Please check out the repository [LICENSE](LICENSE) before using the provided data. 
