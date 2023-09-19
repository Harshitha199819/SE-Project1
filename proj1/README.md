Team 7
Annadurai,Harshitha
Bhoja Ramamanohara,Pannaga Rao
Masineni Prasanna Kumar,Karthik
Niranjana,Prathima Putreddy

C.E.L.T -The Sentiment Analyser
From the get-go, this particular project had us fascinated. Sentiment analysis happens to be a prominent area of research considering its wide range of applications in areas such as social media monitoring, brand reputation research, political analysis and content recommendation among others. Therefore, sentiment analysis , or opinion analysis, is a valuable tool to extract valuable information from data and make crucial data-driven decisions. C.E.L.T, The Sentiment Analyser is a well-designed application with great features that helps users to analyze sentiments not just through text, but also by providing audio, document or a product review link as inputs. All of these caught our attention.

We had a good time setting up and working on this project. However, there were a few obstructions we faced while trying to set up the application on our systems. Below, we have listed a few improvements that could potentially make it easier for others to set up and use the application on their systems.

Some of the required packages were outdated, and the requirements file had to be looked into and modified manually. 
The requirements looked specifically for certain values which were either outdated or not compatible, for instance, “lxml==4.5.2”, was not compatible with the newer versions of some of the other packages. 
How this could have been avoided:
This could have been avoided by using the below practices:
A. Using '>=' or '\~=' instead of == . By using '>=', the Python library will install a version that is either greater than or equal to the mentioned version. This way, it would pick a higher version if a higher version is available. By using '\~=', the library will install a version that is not lesser than the mentioned version, but a compatible version of the same release cycle. For instance, if it said “lxml~=4.5.2”, it could install any compatible version that matches the pattern 4.5.*, but is not less than 4.5.2.
B. The documentation could have mentioned the versions of packages being used. This would have helped the user debug the errors easily without having to look into the codebase. Information on how to fix package incompatibility or package unavailability errors could have also been useful.


Some files used absolute paths for referencing files which caused issues while trying to run the application.
For example, the file https://github.com/mrpudlo/SE_Project1/blob/master/Amazon_Comments_Scrapper/amazon_reviews_scraping/amazon_reviews_scraping/spiders/amazon_review.py , has the below line:
 my_file_handle = open('/Users/sj941/Documents/GitHub/SE_Project1/Amazon_Comments_Scrapper/amazon_reviews_scraping/amazon_reviews_scraping/spiders/ProductAnalysis.txt')

Using an absolute path is not good practice, as it causes issues when the code needs to be reused by others. 
In our case, we saw the “File not found” error multiple times as ‘/Users/sj941/Documents/GitHub’ is a path that is local to someone’s system. 
How this could have been avoided:
Using relative paths to reference files will solve this issue. 


Unclear instructions on accepted input types for file attachments and improper exception catching.

The above input field directs us to upload an audio file. However, the codebase accepts only wav type audio files. When we tried uploading audio files of other types, like of type ogg, it still did not provide an error message that clearly indicated that the error had to do with the file type.
How this could have been avoided:
A. By providing clear directions on what types of files are accepted, and by providing error messages that clearly state the error. 
B. Using client-side form field validations. By using client-side validations, we can check and inform the client whether the input provided is accepted or not, and the client could make the necessary changes even before submitting the form. This is an efficient way to avoid such issues. 


Issues we observed in the other projects:
Requirement files in all other projects had == in place of >= or ~= , which led to a lot of version consistency issues.
In the stock prediction project, the modules were not explained clearly which led to the difficulty in understanding its usability.
Most of the projects did not have details about the fixes being made for the reported bugs.


Here are some practises that we are committing to perform in order to avoid such issues in our Project 2:
Proving clear information about the different packages being used along with their version numbers in the documentation.
Using “>=” or “~=” in the requirements file in order to avoid package incompatibility or unavailability errors at the time of installation.
Using relative paths to reference files in the codebase instead of absolute paths. 
Catching foreseeable errors and providing clear messages for them.
Providing clear instructions on the accepted input types.
To perform form field validation before performing any other operation with the input provided.

By implementing the above practices, we are confident that we can assist users in easily setting up and running applications on their systems.
