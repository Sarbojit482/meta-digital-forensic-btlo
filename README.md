# meta-digital-forensic-btlo
Digital forensics Investigation of the Meta Lab from Blue Team labs online focusing on image metadata and analysis


# Meta – Forensic Investigation
Platform Blue Team Labs Online
Category: Digital Forensics 
Lab Meta

Scenario:The attached images were posted by a criminal on the run, with the caption "I'm roaming free. You will never catch me". We believe you can assist us in proving him wrong.
Investigation Objectives
The investigation required answer for four question
1.	What is the camera Model?
2.	When was the picture taken?
3.	What does the comment on the first image say?
4.	Where could the criminal be?
   
Tools used 
i.	Kali Linux
ii.	Exiftool – image metadata and EXIF analysis
iii.	Picarta.ai – image geolocation analysis

Methodology
1.	Extracting Image metadata
I begain by examining the image using Exiftool:
`command:  exiftool image.jpg`
This provided me with the metadata embedded within the image to be examined

 2.	Identify the camera
The camera manufacturer and model were the identified from the EXIF fields:
Make: Camera Model name
<img width="821" height="591" alt="Screenshot 2026-10-06 234541" src="https://github.com/user-attachments/assets/ad35da7d-48ff-428f-ae07-16e6da39a842" />

 
4.	Determining the Capture time
Examined the Date/Time fild to determin when was the image originally capture
<img width="545" height="62" alt="Screenshot 2026-10-06 235202" src="https://github.com/user-attachments/assets/fa0301f6-af6e-4c39-978f-de16184d608a" />
 
If need a faster way use the command exiftool -DateTimeOriginal Imagename.jpg
 

4.	Investigating the Embedded Comment
The Image metadata was examined for the Comment field:
  
<img width="970" height="432" alt="Screenshot 2026-10-06 235803" src="https://github.com/user-attachments/assets/97fed0a7-c410-4de0-ab61-ed5d663f48ed" />

<br>

5.	Investigate Location
The GPS related meta data was examined using
exiftool -gps:all imagename.jpg
and
exiftool -n -GPSLatitude -GPSLongitude uploaded_1.JPG

Rather then guessing that the meta data is accurate I used

Picarta.ai – image geolocation analysis


Skill Demonstrated
Digital Image Forensics
EXIF metadata extraction
Camera identification
Timestamp analysis
GPS metadata analysis
Evidence interpretation

This investigation demonstrated how seemingly ordinary Photographs can contain valuable forensics information. Also highlighted an important forensic principle: metadata should be treaded as evidence that requires validation, rather than automatically being accepted as ground truth
