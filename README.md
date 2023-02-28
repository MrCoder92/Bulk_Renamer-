# Bulk_Renamer-
Renaming bulk files in a folder or directory 

#For python to know the Operating System you are using (import OS)
import os

#Create the bulk rename function and set i=o (as default)
def main():
    i = 0

#Specify the path/ directory where the bulk file folder is located.
#Change all back slashes to front slash. Put another front slash at the end of the directory URL
#use the for loop to loop through the file and provide the file naming format
    path = "local directory"
    for filename in os.listdir(path):
        my_dest = "img" + str(i) + ".jpg"
        my_source =path + filename
        my_dest =path + my_dest
        os.rename(my_source, my_dest)
        i += 1

#Execute the function
if __name__ == "__main__":
    print(main())
