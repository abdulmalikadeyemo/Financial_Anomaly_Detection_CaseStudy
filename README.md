# **Financial Fraud/Anomaly Detection Case Study**
**Check the python notebook for the complete solution** [Click Here](https://github.com/abdulmalikadeyemo/Financial_Anomaly_Detection_CaseStudy/blob/main/financial_anomaly_detection.ipynb)

## **The Case Study Problem Statement:**

As part of an Audit team of a large company, you are tasked with identifying any irregularities in the company’s general ledger. These irregularities could be anything from an accidental typo (i.e an extra zero) to a calculated fraud. You are assisting the audit team to apply the best of Data Science to form risk-based hypotheses.

&nbsp;

The general ledger houses a company’s accounts and many journal entries are posted to these accounts to either credit or debit balances. When checking journal entries for outliers, typically a rule-based analysis is performed, such as identifying manually entered journals that:

- Do not net to zero
- Are above a particular amount
- Are posted by people that post relatively few journals
- Are round amounts ($32,000)
- Have particular words in the narration (note: the descriptive columns were omitted to preserve the anonymity of the data)
- Are posted by certain people (i.e the CEO)

&nbsp;

Your task is to use any analytical technique of your choice to identify outliers or anomalies in the dataset. It does not have to follow the typical rule-based approach above, but we are most interested in identifying journal postings that do not look like business as usual.


## **The Analytical Approach Solution- The Hypothesis:**

- Given the quality of the dataset provided and the amount of information available, the best approach to detecting anomalous transactions is to use a rule-based analysis.


- From the provided Data Dictionary, It states that the `BAT_NAME` column is an ID for a single journal posting, and all the transactions under a particular BAT_NAME ID must net to zero.


- Concretely, If the journal entries of a BAT_NAME ID is not balanced (i.e, does not net to zero), we can see that journal posting(entry) is anomalous or `not business as usual`


- Hence, our approach is to sum all the `Amount` column entries that belongs to a particular `BAT_NAME` ID and extract all the Journal Posting (Transactions) whoose `Amount` does not net to zero
