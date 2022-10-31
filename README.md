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

A cheque image is taken as an input & scanned. Then this scanned image is transformed into many different small part where every part contain seperate useful information like signature,amount,account number,payee name,bank name,etc.  and these parts that extracted by drawing boxes on those parts of the scanned cheque image that contain these information with help of __OpenCV__ and __Geometry.__
With the help of __Azure APIs__ these small different parts of the scanned images are sent to __OCR(Optical Character Recognition)__ for  processing information written in these small images.
OCR model returns a list of detections and then among that list, there are both useful information and additional informations. Among complete list, detections of only required information are considered(this is  known as __text cleaning or extracting of useful information__).

Please make a note that _Useful information means only that information that is relevant or required for cheque verification and processing._

After cleaning or extracting useful detection from OCR list, the information of the payee is used to match with the payee's existing record information in database __so as to verify if payee is genuine or not__. 

For verifying the identity of the payee, different extracted information is verified like with the help of ML modules, like:

__Signature Verification__ is done with the help of __signver module__ that contains sub-modules like cleaner,extractor,matcher. 



such that signature is sent to signature verification file and  existing gets matched, then it is considered to be verified user. It includes signature verification(using signver module) and verification of details like 
_This whole process is known as verification process and is the most crucial part of the whole process. Only after the successful verification, any processes or transactions(as instructed on cheque like transferring of money to the intended user bank account) takes place._

__After successful cheque processing, the details of the sender gets further updated in the database as per the transaction took place successfully.__
