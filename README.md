# First_script_project
This small project works on archiving data in specific folders, and in order to upload the project I used the git and the terminal to upload the project.


# This little script run to flutter data in the system and put them in specific folders than send me an email message that 
# verify mission is complete

![Screenshot from 2024-10-04 11-34-53](https://github.com/user-attachments/assets/e16a5566-4bdb-4486-abee-58144fc13d26)


![Screenshot from 2024-10-04 11-42-10](https://github.com/user-attachments/assets/14af64db-0136-4b4f-bbc5-bcf40afaf332)

![Screenshot from 2024-10-04 11-50-50](https://github.com/user-attachments/assets/c03607e5-8e1c-4b4d-89b5-e445342158d0)



import os 
import shutil
import smtplib

# Organize images in to Image diractery

def organize():
    
    file_path = os.path.dirname(os.path.realpath(__file__))

    for filename in os.listdir(file_path):
        if filename.endswith(("png","gpg","ipeg","gif","icon","ipg")):
            if not os.path.exists("Images") :
                os.mkdir("Images")
            shutil.copy(filename , "Images")
            os.remove(filename)
            print("Organizing Images Done")
organize()


# Organize videos in to video diractery

def organize1():
    
    file_path = os.path.dirname(os.path.realpath(__file__))

    for filename in os.listdir(file_path):
        if filename.endswith(("mp4","mpvf")):
            if not os.path.exists("Videos") :
                os.mkdir("Videos")
            shutil.copy(filename , "Videos")
            os.remove(filename)
            print("Organizing Videos Done")
organize1()

# Organize documents in to document diractery


def organize2():
    
    file_path = os.path.dirname(os.path.realpath(__file__))

    for filename in os.listdir(file_path):
        if filename.endswith(("pdf","docx","zip","pptx","ppt","txt")):
            if not os.path.exists("Documents") :
                os.mkdir("Documents")
            shutil.copy(filename , "Documents")
            os.remove(filename)
            print("Organizing Documents Done")
organize2()

# Organize audios in to audio diractery


def organize3():
    
    file_path = os.path.dirname(os.path.realpath(__file__))

    for filename in os.listdir(file_path):
        if filename.endswith(("mp3","m4a")):
            if not os.path.exists("Audios") :
                os.mkdir("Audios")
            shutil.copy(filename , "Audios")
            os.remove(filename)
            print("Organizing Audios Done")
organize3()

# Organize code files in to code file diractery

def organize4():
    
    file_path = os.path.dirname(os.path.realpath(__file__))

    for filename in os.listdir(file_path):
        if filename.endswith(("py","html","js","bash")):
            if not os.path.exists("Codes") :
                os.mkdir("Codes")
            shutil.copy(filename , "Codes")
            os.remove(filename)
            print("Organizing Codes Done")
organize4()

# sending email message to conform process is done

def notiefy_me():

    server =smtplib.SMTP("smtp.gmail.com",587)
    server.starttls()
    server.login("fysalhassan159@gmail.com","jaevsHng4U54")
    server.sendmail("fysalhassan159@gmail.com","faisalhassan159159@gmail.com","organizing your data is done")

notiefy_me()

