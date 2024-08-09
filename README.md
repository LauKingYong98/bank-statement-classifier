# bank-statement-classifier
---
A project to deploy a fine-tuned Transfomers Encoder model for classification tasks on bank statement transactions to automate repetitive daily bank posting tasks.
### Project Background
There are a lot of repetitive activities in daily accounting tasks, specifically in record to report function. One of it is perform daily bank posting. Timely bank posting acts as an internal control mechanism to maintain accurate financial record of organisation. Bank reconciliation are performed after bank posting to match bank statement with bank GL, and any discrepancies can be identified and rectified. Treasury team might need to use current balance for forex hedging analysis/ transactions. 
### Scope Of Work
In this project, I developed a neural network model to perform classification tasks on bank statement. This is the first part of full bank automation cycle, where we extract details from the bank statements downloaded from bank portal into tabular data format, and fetched the input into fine-tuned model to return classified labels. The output labels will then be integrated into a VBA-based bank automation workfile to identify the correct GL account code to automatically generate bank posting template and uploaded to any ERP/ accouting software. 

This project is a documentation of fine-tuning a pre-trained BERT model to perform classification tasks. The following areas are covered:
1. Data preparation through ETL process by using Pandas module.
2. Featue engineering on dataset to simplify input data structure to enhance model accuracy.
3. Fine tune pre-trained encoder model and evaluate the accuracy.
4. Deploy the model.

### Result
The fine-tuned model are able to achieve an accuracy of 99.85% in testing set and 99.55% on subsequent actual transactions from bank statements.

Training Set:
| Epoch | Training Loss | Validation Loss | Accuracy 
| ---- | ---- | ---- | ---- |
| 1	| 0.045200	|0.033498	|0.989474|
|2	|0.016100	|0.009197	|0.998496|
|3	|0.007900	|0.008938	|0.998747|

Actual Dataset from Bank Statements:
| Remark | Count | Percentage |
| ---- | ---- | ---- |
| FALSE | 17 | 0.45% |
| TRUE | 3753 | 99.55% |
|TOTAL | 3770 | 100% |
