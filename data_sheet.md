# Datasheet Template

## Motivation

- For what purpose was the dataset created? <br> The dataset was created by an individual with an interest in horse racing, in hopes of finding like-minded data scientists.
- Who created the dataset (e.g., which team, research group) and on behalf of which entity (e.g., company, institution, organization)? Who funded the creation of the dataset? <br>
The dataset was created by an individual, on behalf of no entity and with no funding.

 
## Composition

- What do the instances that comprise the dataset represent (e.g., documents, photos, people, countries)? <br>
There are two files: races.csv, where each instance represents the conditions of an individual race, and runs.csv, where each instance represents the characteristics of one horse run.
- How many instances of each type are there? <br>
There are 6,349 instances in races.csv, and 79,447 instances in runs.csv.
- Is there any missing data? <br>
In my initial analysis, I found two instances with missing data, when joining races and runs on the race_id column.
- Does the dataset contain data that might be considered confidential (e.g., data that is protected by legal privilege or by    doctor–patient confidentiality, data that includes the content of individuals’ non-public communications)? <br>
No, all identifying data was removing in pre-processing.

## Collection process

- How was the data acquired? <br>
Unspecified free resources
- If the data is a sample of a larger subset, what was the sampling strategy? <br>
Not specified
- Over what time frame was the data collected? <br>
Not specified

## Preprocessing/cleaning/labelling

- Was any preprocessing/cleaning/labeling of the data done (e.g., discretization or bucketing, tokenization, part-of-speech tagging, SIFT feature extraction, removal of instances, processing of missing values)? If so, please provide a description. If not, you may skip the remaining questions in this section. <br>
Personally-identifiable information, such as horse and jockey names, were excluded.
- Was the “raw” data saved in addition to the preprocessed/cleaned/labeled data (e.g., to support unanticipated future uses)? <br>
No.
 
## Uses

- What other tasks could the dataset be used for? 
- Is there anything about the composition of the dataset or the way it was collected and preprocessed/cleaned/labeled that might impact future uses? For example, is there anything that a dataset consumer might need to know to avoid uses that could result in unfair treatment of individuals or groups (e.g., stereotyping, quality of service issues) or other risks or harms (e.g., legal risks, financial harms)? If so, please provide a description. Is there anything a dataset consumer could do to mitigate these risks or harms? <br>
Personally identifiable information was removed, leaving only the horse's country that could result in potential stereotyping. I do not forsee potential issues with the remaining data.
- Are there tasks for which the dataset should not be used? If so, please provide a description. <br>
Not that I can think of.

## Distribution

- How has the dataset already been distributed? <br>
Via Kaggle.
- Is it subject to any copyright or other intellectual property (IP) license, and/or under applicable terms of use (ToU)? <br>
Not specified. 

## Maintenance

- Who maintains the dataset? <br>
There is no specified unkeep. 

