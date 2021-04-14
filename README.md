# Mini-Assistent

import webbrowser as browser #if not installed open the terminal or Command prompt (cmd) and type "pip install webbrowser" and then press enter  
  
my_browser = browser.get('windows-default')  
  
  
recunoastere = ["Alice", "open", "search"] #Start & command: first word have to be Alice (like "hello google") and second word have to be open or search.  
  
ComandaOpen = ["youtube", "facebook", "instagram"] #For "open" command. What you want to open(ex: Alice open youtube)  
x = input()  
x = x.split(" ") #Transform your input into a list(to be easier later)  
  
if recunoastere[0] == x[0]: #Check if first word of your input matches with "Alice", if yes then:<br/>
    if recunoastere[1] == x[1]: #Check if your second word is "open", if yes then:  <br/>
        if ComandaOpen[0] == x[2]:#Check if your third word is "youtube", if yes then:  
            my_browser.open_new("https://www.youtube.com/") #Open youtube  
        if ComandaOpen[1] == x[2]:#Check if your third word is "facebook", if yes then:  
            my_browser.open_new("https://www.facebook.com/") #Open facebook  
        if ComandaOpen[2] == x[2]:#Check if your third word is "instagram", if yes then:  
            my_browser.open_new("https://www.instagram.com/")#open instagram  
    elif recunoastere[2] == x[1]:#Check if your second word is "search", if yes then:  
        x.remove(x[0]) #remove the word "Alice" from your input  
        x.remove(x[0]) #remove the word "search" from your input  
        url= "https://www.youtube.com/results?search_query=" #set the youtube search template.  
        for i in range(len(x)): #Make a for loop to search the remaing words on youtube   
            url = url + f"+{x[0]}" #add the first word to template (url)  
            x.remove(x[0]) #remove the word what was just added to template  
        my_browser.open_new(url) #open the link  
#1st ex : Alice search be cu mine        --> https://www.youtube.com/results?search_query=be+cu+mine  
#2nd ex : Alice open facebook            --> https://www.facebook.com/  
#3rd ex : Alice open youtube             --> https://www.youtube.com/  
  
#I hope you enjoy my work <3  
#https://github.com/HaosKid  
