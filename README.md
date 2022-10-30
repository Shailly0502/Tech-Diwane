A solution is provided for the given Problem Statement.

# Problem Statement

Bank handles large volumes of cheques in the clearing process. The process involves many technical verifications including signature verification. Some of these steps are manual and require human intervention to complete the process. The current process requires the high human capital deployment and longer processing time.

# Expected Solution

Using rule-based and AI/ML/ICR/ OCR (Optical Character Recognition) capabilities for automation and doing technical and signature verification of the cheques.
* Automation of the clearing process using AI/ML/ICR/OCR techniques
* Automatic Data Entry & Technical verification
* Signature Verification
* Support Multilingual
* Reduce Human Efforts
* Reduce Processing time
* Detecting Potential Frauds

# Proposed Solution

Firstly, a cheque is taken as an input and then different boxes are drawn and then it is sent to OCR model through APIs. Then OCR model returns a list of detections and then useful information is extracted from that list. Then that extracted information is being matched with the existing records of user's bank details and if both information gets match, then further action like processing of amount that is written on cheque is transferred to intented user bank account and details of the user gets updated in the database.
