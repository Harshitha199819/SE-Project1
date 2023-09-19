## Team 7
Team members: <br>
Annadurai,Harshitha <br>
Bhoja Ramamanohara,Pannaga Rao <br>
Masineni Prasanna Kumar,Karthik <br>
Niranjana,Prathima Putreddy <br>

## NAVIGATION LINKS:
### ESSAY 
Present in the README file under navigation links. [Read essay](https://github.com/Harshitha199819/SE-Project1/blob/main/proj1/README.md#essay-1)

### YOUTUBE VIDEO OF WORKING VIDEO 
[Watch YouTube video](https://www.youtube.com/watch?v=V5RYZG6PYrQ)

### PROJECT GRADING 
[Go to project gradings folder](https://github.com/Harshitha199819/SE-Project1/tree/main/proj1/project%20gradings)
[How is the project gradings folder structures?](https://github.com/Harshitha199819/SE-Project1/edit/main/proj1/README.md#note)

### NOTE 
project gradings folder has 6 files. <br>
The individual <project_name>.csv files are files containing the grades for each project assigned to us. <br>
project 1.xlsx is a combined file containing grades of all files in different sheets. (This file has the same content as the individual files) <br>


## ESSAY:

From the get-go, C.E.L.T -The Sentiment Analyser, had us fascinated. Sentiment analysis happens to be a prominent area of research considering its wide range of applications in areas such as social media monitoring, brand reputation research, political analysis and content recommendation among others. Therefore, sentiment analysis , or opinion analysis, is a valuable tool to extract information from data and make crucial data-driven decisions. C.E.L.T, The Sentiment Analyser is a well-designed application with great features that helps users to analyze sentiments not just through text, but also by providing audio, document or a product review link as inputs. All of these caught our attention.
<br>
We had a good time setting up and working on this project. However, there were a few obstructions we faced while trying to set up the application on our systems. Below, we have listed a few improvements that could potentially make it easier for others to set up and use the application on their systems.
<br>
### Some of the required packages were outdated, and the requirements file had to be looked into and modified manually. 
The requirements looked specifically for certain values which were either outdated or not compatible, for instance, “lxml==4.5.2”, was not compatible with the newer versions of some of the other packages. <br>
How this could have been avoided:<br>
This could have been avoided by using the below practices:<br>
A. Using '>=' or '\~=' instead of == . By using '>=', the Python library will install a version that is either greater than or equal to the mentioned version. This way, it would pick a higher version if a higher version is available. By using '\~=', the library will install a version that is not lesser than the mentioned version, but a compatible version of the same release cycle. For instance, if it said “lxml~=4.5.2”, it could install any compatible version that matches the pattern 4.5.*, but is not less than 4.5.2. <br>
B. The documentation could have mentioned the versions of packages being used. This would have helped the user debug the errors easily without having to look into the codebase. Information on how to fix package incompatibility or package unavailability errors could have also been useful.


### Some files used absolute paths for referencing files which caused issues while trying to run the application.
For example, the file https://github.com/mrpudlo/SE_Project1/blob/master/Amazon_Comments_Scrapper/amazon_reviews_scraping/amazon_reviews_scraping/spiders/amazon_review.py , has the below line: <br>
 my_file_handle = open('/Users/sj941/Documents/GitHub/SE_Project1/Amazon_Comments_Scrapper/amazon_reviews_scraping/amazon_reviews_scraping/spiders/ProductAnalysis.txt')
<br>
Using an absolute path is not good practice, as it causes issues when the code needs to be reused by others. 
In our case, we saw the “File not found” error multiple times as ‘/Users/sj941/Documents/GitHub’ is a path that is local to someone’s system. <br>
How this could have been avoided: <br>
Using relative paths to reference files will solve this issue. 


### Unclear instructions on accepted input types for file attachments and improper exception catching
<br>
![Screenshot (19)](https://github.com/Harshitha199819/SE-Project1/assets/47849112/4ab59f87-f88f-4728-abf8-cd1a176aa7ed)

The above input field directs us to upload an audio file. However, the codebase accepts only wav type audio files. When we tried uploading audio files of other types, like of type ogg, it still did not provide an error message that clearly indicated that the error had to do with the file type.
How this could have been avoided:
A. By providing clear directions on what types of files are accepted, and by providing error messages that clearly state the error. 
B. Using client-side form field validations. By using client-side validations, we can check and inform the client whether the input provided is accepted or not, and the client could make the necessary changes even before submitting the form. This is an efficient way to avoid such issues. 


Issues we observed in the other projects:<br>
Requirement files in all other projects had == in place of >= or \~= , which led to a lot of version consistency issues.<br>
In the stock prediction project, the modules were not explained clearly which led to the difficulty in understanding its usability.<br>
Most of the projects did not have details about the fixes being made for the reported bugs.<br>


Here are some practises that we are committing to perform in order to avoid such issues in our Project 2: <br>
1. Proving clear information about the different packages being used along with their version numbers in the documentation.<br>
2. Using “>=” or “\~=” in the requirements file in order to avoid package incompatibility or unavailability errors at the time of installation.<br>
3. Using relative paths to reference files in the codebase instead of absolute paths. <br>
4. Catching foreseeable errors and providing clear messages for them.<br>
5. Providing clear instructions on the accepted input types.<br>
6. To perform form field validation before performing any other operation with the input provided.<br>

By implementing the above practices, we are confident that we can assist users in easily setting up and running applications on their systems.
