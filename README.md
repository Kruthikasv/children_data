# children_data
Organization of children data

There are two types of users we'll call them anonymous and named 
I have extracted information about each user from the metadata and stored it in the xl 
I useed regular expressions to extract said data
Once the data has been extracted and stored in the xl, we use the xl to create directories that store uniquely identified data of each user 
The directories are made in the below format:
UniqueID_UserName -> Audio_folder        -> language -> audio_files
                  -> Images or Sentences -> language -> respective images/ a text file with sentences
Please note that the languages 'bengali', 'english', 'hindi', 'kannada', 'marathi', 'tamil', 'telugu' are the only languaes that had sentence promts the users got image promts for the other languages.
