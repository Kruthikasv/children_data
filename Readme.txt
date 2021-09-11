# children_data
Organization of children data
Research intern in SPIRE LAB, IISc

There are two types of users we'll call them anonymous and named.
This code extracts information about each user from the metadata and stores it in the xl as well as creates directories for each user that contains the audio files and sentences(or)images associated with the audio files.
 
The directories are made in the below format:
StudentID_UserName -> Audio_folder        -> language -> audio_files
                  -> Images or Sentences -> language -> respective images or a text file with sentences

Note: The languages 'bengali', 'english', 'hindi', 'kannada', 'marathi', 'tamil', 'telugu' are the only languaes that have sentence promts, the users got image promts for the other languages.

def matching_audio :
Here, I am matching the different audio files done by a single user and saving it as a dictiorany. I am matching the audio files by comparing the unique ID of the user.

def extraction :
In this function the information of each user is extracted from the metadata by searching for the user_name and then storing it as a list.

def search_attributes :
Once all the usere's data is extracted in the previous function, in this function I used regular expressions to match and extract required data such as name, email, phno etc and store it in a list. 

def save_data :
After extracting the attributes of all required data, in this function the extracted data is saved/appended into an xl file under the respective columns for each anonymous user.

def save_data_named :
This function is similar to the previous function, but this is storing the data of named users in another sheet of the same xl.

def user_data :
In this function I am extracting the name, age, providerID and subjectID of each user and storing it as a list.

def age_classification :
Using the list created in the previous function, here I am dividing the users based on their age. That is, users below the age of 12 are stored in a separate list than the users above the age of 12.

def language :
In this function, the sentences of each language is extracted from the metadata file and stored as a list and this list is then appended to a dictionary under their respective languages.

def count_recordings :
This function is used to count the total number of different recordings made by each user as well as display the path for each audio file.

def make_directories :
In this function, the directories for each user above the age of 12 is created. The format of the crated directories is mentioned above.
Users above the age of 12 were showed either sentence promts or image promts based on the language they selected. 
To know which languages got the sentence and image prompts respectively please read the "Note" written above.

def make_directories2 :
In this function, the directories for each user below the age of 12 is created. The format of the crated directories is mentioned above.
All users below the age of 12 were given only image prompts irrespective of the language they chose. 

def audio_folder :
Here, the audio files of a particular user which are stored in a common folder containg all audio files of users is copied to the respective folder created for that particular user.

def update_workbook :
Once the directories are made and the audio files of each users are stored respectively, the xl containg data of each user is updated by adding a column with the name of the folder created for each user. The name of the folder is in the format "studentID_username"

def delete_copies :
This function deletes the folders every time the code is run to prevent from having redundant/repeating information.

